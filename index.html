<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AIM Chatroom</title>
    <!-- Tailwind CSS CDN for easy styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Inter font for a clean modern look -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Custom styles to override or enhance Tailwind */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f2f5; /* Light grey background */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 1rem; /* Padding for mobile views */
            box-sizing: border-box;
        }

        .container {
            background-color: #ffffff;
            border-radius: 1rem; /* Rounded corners for the main container */
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            overflow: hidden; /* Ensures rounded corners apply to children */
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 40rem; /* Max width for desktop */
            height: 90vh; /* Occupy most of the viewport height */
            max-height: 45rem; /* Max height for desktop */
            position: relative; /* For absolute positioning of modal */
        }

        .chat-header {
            background-color: #4a90e2; /* AOL-like blue */
            color: white;
            padding: 1rem 1.5rem;
            border-top-left-radius: 1rem;
            border-top-right-radius: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-weight: 600;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            z-index: 10; /* Ensure header is above chat */
        }

        .chat-messages {
            flex-grow: 1;
            padding: 1.5rem;
            overflow-y: auto; /* Scrollable chat area */
            display: flex;
            flex-direction: column;
            gap: 0.75rem; /* Space between messages */
            background-color: #e6f0fa; /* Very light blue for chat background */
        }

        .message-bubble {
            max-width: 80%;
            padding: 0.75rem 1rem;
            border-radius: 0.75rem; /* Rounded message bubbles */
            word-wrap: break-word; /* Break long words */
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.08);
        }

        .message-bubble.sent {
            background-color: #d4edda; /* Light green for sent messages */
            align-self: flex-end; /* Align to right */
            color: #28a745; /* Darker green text */
        }

        .message-bubble.received {
            background-color: #ffffff; /* White for received messages */
            align-self: flex-start; /* Align to left */
            color: #333;
        }

        .message-username {
            font-weight: 600;
            font-size: 0.875rem; /* Smaller font for username */
            margin-bottom: 0.25rem;
            color: #4a90e2; /* Blue for username */
        }

        .chat-input-area {
            display: flex;
            padding: 1rem 1.5rem;
            background-color: #f8f9fa; /* Light grey for input area */
            border-top: 1px solid #e0e0e0;
            gap: 0.75rem; /* Space between input and button */
        }

        .chat-input {
            flex-grow: 1;
            padding: 0.75rem 1rem;
            border: 1px solid #cccccc;
            border-radius: 0.75rem;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.2s;
        }

        .chat-input:focus {
            border-color: #4a90e2;
        }

        .btn {
            padding: 0.75rem 1.25rem;
            border-radius: 0.75rem;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s, transform 0.1s;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .btn-primary {
            background-color: #4a90e2;
            color: white;
        }

        .btn-primary:hover {
            background-color: #3a7bd5;
            transform: translateY(-1px);
        }

        .btn-secondary {
            background-color: #f0f0f0;
            color: #333;
            border: 1px solid #ccc;
        }

        .btn-secondary:hover {
            background-color: #e0e0e0;
            transform: translateY(-1px);
        }

        /* Login Modal Styles */
        .modal-overlay {
            position: absolute; /* Changed to absolute for container relative positioning */
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.6); /* Darker overlay */
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 20; /* Above chat content */
        }

        .modal-content {
            background-color: #ffffff;
            padding: 2rem;
            border-radius: 1rem;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            width: 90%;
            max-width: 28rem; /* Max width for modal */
            text-align: center;
            display: flex;
            flex-direction: column;
            gap: 1.25rem;
        }

        .modal-input {
            width: 100%;
            padding: 0.75rem 1rem;
            border: 1px solid #cccccc;
            border-radius: 0.75rem;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.2s;
        }

        .modal-input:focus {
            border-color: #4a90e2;
        }

        .error-message {
            color: #dc3545; /* Red for errors */
            font-size: 0.875rem;
            margin-top: -0.5rem;
        }

        .hidden {
            display: none !important;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .container {
                height: 100vh; /* Full height on smaller screens */
                max-height: unset; /* Remove max-height constraint */
                border-radius: 0; /* No rounded corners on full screen */
            }
            body {
                padding: 0; /* No padding on body for full screen app */
            }
            .chat-header, .chat-input-area {
                padding: 0.75rem 1rem;
            }
            .chat-messages {
                padding: 1rem;
            }
            .message-bubble {
                padding: 0.6rem 0.8rem;
            }
            .modal-content {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div id="app" class="container">
        <!-- Chat Header -->
        <div class="chat-header">
            <span id="current-user-display">AIM Chatroom</span>
            <button id="logout-button" class="btn btn-secondary text-sm px-3 py-1.5 hidden">Logout</button>
        </div>

        <!-- Chat Messages Area -->
        <div id="chat-messages" class="chat-messages">
            <!-- Messages will be dynamically added here -->
        </div>

        <!-- Chat Input Area -->
        <div class="chat-input-area">
            <input type="text" id="message-input" class="chat-input" placeholder="Type your message...">
            <button id="send-button" class="btn btn-primary">Send</button>
        </div>

        <!-- Login/Signup Modal -->
        <div id="login-modal" class="modal-overlay">
            <div class="modal-content">
                <h2 class="text-2xl font-bold text-gray-800">Welcome to AIM Chat!</h2>
                <p class="text-gray-600">Please login or create an account to join the chat.</p>

                <input type="email" id="auth-email" class="modal-input" placeholder="Email">
                <input type="password" id="auth-password" class="modal-input" placeholder="Password">
                <p id="auth-error-message" class="error-message hidden"></p>

                <button id="login-button" class="btn btn-primary">Login</button>
                <button id="signup-button" class="btn btn-secondary">Sign Up</button>
            </div>
        </div>
    </div>

    <!-- Supabase JS CDN -->
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
    <script>
        // IMPORTANT: Replace these with your actual Supabase project URL and Anon Key
        // You will get these from your Supabase project settings (Project Settings -> API)
        const SUPABASE_URL = 'https://seqbgjemyohwkrarrqei.supabase.co'; // e.g., 'https://abcde12345.supabase.co'
        const SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InNlcWJnamVteW9od2tyYXJycWVpIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTE0Mzk0NDcsImV4cCI6MjA2NzAxNTQ0N30.u0De17tt6t6l6MHnn_wB6tMiZhFskwrtcM0GaMGyuXE'; // e.g., 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...'

        // Initialize Supabase client
        const supabase = Supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);

        // Get DOM elements
        const loginModal = document.getElementById('login-modal');
        const chatMessagesDiv = document.getElementById('chat-messages');
        const messageInput = document.getElementById('message-input');
        const sendButton = document.getElementById('send-button');
        const logoutButton = document.getElementById('logout-button');
        const authEmailInput = document.getElementById('auth-email');
        const authPasswordInput = document.getElementById('auth-password');
        const loginButton = document.getElementById('login-button');
        const signupButton = document.getElementById('signup-button');
        const authErrorMessage = document.getElementById('auth-error-message');
        const currentUserDisplay = document.getElementById('current-user-display');

        let currentUserId = null;
        let currentUserEmail = null;

        /**
         * Displays an error message in the authentication modal.
         * @param {string} message - The error message to display.
         */
        function showAuthError(message) {
            authErrorMessage.textContent = message;
            authErrorMessage.classList.remove('hidden');
        }

        /**
         * Clears the error message in the authentication modal.
         */
        function clearAuthError() {
            authErrorMessage.classList.add('hidden');
            authErrorMessage.textContent = '';
        }

        /**
         * Handles user login.
         */
        async function handleLogin() {
            clearAuthError();
            const email = authEmailInput.value;
            const password = authPasswordInput.value;

            if (!email || !password) {
                showAuthError('Please enter both email and password.');
                return;
            }

            try {
                const { error } = await supabase.auth.signInWithPassword({ email, password });
                if (error) throw error;
                // UI will be updated by onAuthStateChange listener
            } catch (error) {
                console.error('Login error:', error.message);
                showAuthError(`Login failed: ${error.message}`);
            }
        }

        /**
         * Handles user signup.
         */
        async function handleSignup() {
            clearAuthError();
            const email = authEmailInput.value;
            const password = authPasswordInput.value;

            if (!email || !password) {
                showAuthError('Please enter both email and password.');
                return;
            }

            try {
                const { error } = await supabase.auth.signUp({ email, password });
                if (error) throw error;
                // Supabase sends a confirmation email.
                showAuthError('Sign up successful! Please check your email to confirm your account, then you can log in.');
                // Optionally, you might want to disable the signup button or show a success message
            } catch (error) {
                console.error('Signup error:', error.message);
                showAuthError(`Signup failed: ${error.message}`);
            }
        }

        /**
         * Handles user logout.
         */
        async function handleLogout() {
            try {
                const { error } = await supabase.auth.signOut();
                if (error) throw error;
                // UI will be updated by onAuthStateChange listener
            } catch (error) {
                console.error('Logout error:', error.message);
                // Optionally display a message to the user
            }
        }

        /**
         * Fetches and displays existing chat messages.
         */
        async function fetchMessages() {
            try {
                const { data: messages, error } = await supabase
                    .from('messages')
                    .select('*')
                    .order('created_at', { ascending: true });

                if (error) throw error;

                chatMessagesDiv.innerHTML = ''; // Clear existing messages
                messages.forEach(addMessageToChat);
                scrollToBottom();
            } catch (error) {
                console.error('Error fetching messages:', error.message);
            }
        }

        /**
         * Adds a single message to the chat display.
         * @param {object} message - The message object from Supabase.
         */
        function addMessageToChat(message) {
            const messageBubble = document.createElement('div');
            messageBubble.classList.add('message-bubble');

            // Determine if the message was sent by the current user
            const isSentByCurrentUser = message.user_id === currentUserId;
            messageBubble.classList.add(isSentByCurrentUser ? 'sent' : 'received');

            const usernameSpan = document.createElement('div');
            usernameSpan.classList.add('message-username');
            usernameSpan.textContent = message.username || 'Anonymous'; // Display username or 'Anonymous'

            const contentP = document.createElement('p');
            contentP.textContent = message.content;

            messageBubble.appendChild(usernameSpan);
            messageBubble.appendChild(contentP);
            chatMessagesDiv.appendChild(messageBubble);
            scrollToBottom();
        }

        /**
         * Sends a new message to the database.
         */
        async function sendMessage() {
            const content = messageInput.value.trim();
            if (!content || !currentUserId) return; // Don't send empty messages or if not logged in

            try {
                const { error } = await supabase.from('messages').insert([
                    {
                        user_id: currentUserId,
                        username: currentUserEmail, // Use email as username for simplicity
                        content: content
                    }
                ]);

                if (error) throw error;

                messageInput.value = ''; // Clear input field
                scrollToBottom(); // Scroll to bottom after sending
            } catch (error) {
                console.error('Error sending message:', error.message);
            }
        }

        /**
         * Scrolls the chat messages div to the bottom.
         */
        function scrollToBottom() {
            chatMessagesDiv.scrollTop = chatMessagesDiv.scrollHeight;
        }

        /**
         * Sets up the real-time subscription for new messages.
         */
        function setupRealtimeSubscription() {
            supabase
                .channel('public:messages') // Channel name, can be anything unique
                .on(
                    'postgres_changes',
                    { event: 'INSERT', schema: 'public', table: 'messages' },
                    (payload) => {
                        console.log('New message received!', payload.new);
                        addMessageToChat(payload.new);
                    }
                )
                .subscribe();
        }

        // Event Listeners
        loginButton.addEventListener('click', handleLogin);
        signupButton.addEventListener('click', handleSignup);
        logoutButton.addEventListener('click', handleLogout);
        sendButton.addEventListener('click', sendMessage);
        messageInput.addEventListener('keydown', (e) => {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });

        // Supabase Auth State Change Listener
        supabase.auth.onAuthStateChange((event, session) => {
            if (event === 'SIGNED_IN' && session) {
                currentUserId = session.user.id;
                currentUserEmail = session.user.email;
                currentUserDisplay.textContent = `AIM Chatroom - Logged in as: ${currentUserEmail}`;
                loginModal.classList.add('hidden'); // Hide login modal
                logoutButton.classList.remove('hidden'); // Show logout button
                fetchMessages(); // Fetch messages for the logged-in user
                setupRealtimeSubscription(); // Start real-time listener
                messageInput.focus(); // Focus on message input
            } else {
                currentUserId = null;
                currentUserEmail = null;
                currentUserDisplay.textContent = 'AIM Chatroom';
                loginModal.classList.remove('hidden'); // Show login modal
                logoutButton.classList.add('hidden'); // Hide logout button
                chatMessagesDiv.innerHTML = ''; // Clear chat messages
                // Optionally, unsubscribe from real-time if needed, though Supabase handles it on sign out.
            }
            clearAuthError(); // Clear any previous auth errors
        });

        // Initial check for session on page load (important for persistent login)
        // The onAuthStateChange listener above will handle the initial session check automatically,
        // but it's good practice to ensure the UI reflects the state immediately.
        // The `getSession` call is often used for explicit checks if `onAuthStateChange` isn't enough.
        // For this simple app, `onAuthStateChange` is sufficient.
    </script>
</body>
</html>
