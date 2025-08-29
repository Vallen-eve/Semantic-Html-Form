# Semantic-Html-Form
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Registration Form</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7f9;
            color: #333;
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }
        
        .description {
            color: #7f8c8d;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }
        
        .form-section {
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eaeaea;
        }
        
        h2 {
            color: #3498db;
            margin-bottom: 15px;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
        }
        
        h2::after {
            content: "";
            flex-grow: 1;
            height: 1px;
            background: #eaeaea;
            margin-left: 15px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
        }
        
        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="password"],
        select,
        textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        input:focus,
        select:focus,
        textarea:focus {
            border-color: #3498db;
            outline: none;
            box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.2);
        }
        
        .radio-group, .checkbox-group {
            margin-top: 8px;
        }
        
        .radio-option, .checkbox-option {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .radio-option input, .checkbox-option input {
            margin-right: 10px;
        }
        
        .required {
            color: #e74c3c;
        }
        
        .help-text {
            font-size: 0.85rem;
            color: #7f8c8d;
            margin-top: 5px;
        }
        
        button {
            background: #3498db;
            color: white;
            border: none;
            padding: 14px 28px;
            font-size: 18px;
            border-radius: 6px;
            cursor: pointer;
            transition: background 0.3s;
            font-weight: 600;
            display: block;
            margin: 30px auto 10px;
            width: 100%;
            max-width: 250px;
        }
        
        button:hover {
            background: #2980b9;
        }
        
        footer {
            text-align: center;
            margin-top: 30px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>User Registration Form</h1>
            <p class="description">Please fill out this form with the required information</p>
        </header>

        <form method="post" action="#">
            <!-- Personal Information Section -->
            <section class="form-section">
                <h2>Personal Information</h2>
                
                <div class="form-group">
                    <label for="fullname">Full Name <span class="required">*</span></label>
                    <input type="text" id="fullname" name="fullname" required aria-required="true">
                </div>
                
                <div class="form-group">
                    <label for="email">Email Address <span class="required">*</span></label>
                    <input type="email" id="email" name="email" required aria-required="true">
                    <p class="help-text">Please enter a valid email address</p>
                </div>
                
                <div class="form-group">
                    <label for="phone">Phone Number</label>
                    <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" placeholder="Format: 123-456-7890">
                </div>
                
                <div class="form-group">
                    <label for="dob">Date of Birth</label>
                    <input type="text" id="dob" name="dob" placeholder="MM/DD/YYYY">
                </div>
            </section>

            <!-- Account Information Section -->
            <section class="form-section">
                <h2>Account Information</h2>
                
                <div class="form-group">
                    <label for="username">Username <span class="required">*</span></label>
                    <input type="text" id="username" name="username" required aria-required="true">
                    <p class="help-text">Must be 5-15 characters long</p>
                </div>
                
                <div class="form-group">
                    <label for="password">Password <span class="required">*</span></label>
                    <input type="password" id="password" name="password" required aria-required="true">
                    <p class="help-text">Must contain at least one number and one uppercase letter</p>
                </div>
                
                <div class="form-group">
                    <label for="confirm-password">Confirm Password <span class="required">*</span></label>
                    <input type="password" id="confirm-password" name="confirm-password" required aria-required="true">
                </div>
            </section>

            <!-- Preferences Section -->
            <section class="form-section">
                <h2>Preferences</h2>
                
                <div class="form-group">
                    <label>Communication Preferences</label>
                    <div class="checkbox-group">
                        <div class="checkbox-option">
                            <input type="checkbox" id="email-news" name="comm-pref" value="email-news">
                            <label for="email-news">Email Newsletter</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" id="sms" name="comm-pref" value="sms">
                            <label for="sms">SMS Updates</label>
                        </div>
                        <div class="checkbox-option">
                            <input type="checkbox" id="push" name="comm-pref" value="push">
                            <label for="push">Push Notifications</label>
                        </div>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="theme">Theme Preference</label>
                    <select id="theme" name="theme">
                        <option value="">Please select</option>
                        <option value="light">Light</option>
                        <option value="dark">Dark</option>
                        <option value="system">Use System Setting</option>
                    </select>
                </div>
            </section>

            <!-- Additional Information Section -->
            <section class="form-section">
                <h2>Additional Information</h2>
                
                <div class="form-group">
                    <label for="bio">Short Bio</label>
                    <textarea id="bio" name="bio" rows="4" placeholder="Tell us a little about yourself"></textarea>
                </div>
                
                <div class="form-group">
                    <label>How did you hear about us?</label>
                    <div class="radio-group">
                        <div class="radio-option">
                            <input type="radio" id="friend" name="referral" value="friend">
                            <label for="friend">Friend or Colleague</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="search" name="referral" value="search">
                            <label for="search">Search Engine</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="social" name="referral" value="social">
                            <label for="social">Social Media</label>
                        </div>
                        <div class="radio-option">
                            <input type="radio" id="other" name="referral" value="other">
                            <label for="other">Other</label>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Terms and Submission -->
            <section class="form-section">
                <div class="form-group">
                    <div class="checkbox-option">
                        <input type="checkbox" id="terms" name="terms" required aria-required="true">
                        <label for="terms">I agree to the Terms and Conditions <span class="required">*</span></label>
                    </div>
                </div>
                
                <button type="submit">Create Account</button>
            </section>
        </form>

        <footer>
            <p>© 2023 Example Company. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>
