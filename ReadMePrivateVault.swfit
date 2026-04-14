import SwiftUI

struct PrivateVaultIntroView: View {
    var body: some View {
        ScrollView {
            VStack(spacing: 24) {
                
                // Logo
                Image("logo")
                    .resizable()
                    .scaledToFit()
                    .frame(width: 110, height: 110)
                    .clipShape(RoundedRectangle(cornerRadius: 24, style: .continuous))
                    .shadow(radius: 10)
                    .padding(.top, 20)
                
                // Title + subtitle
                VStack(spacing: 10) {
                    Text("Private Vault – Offline Safe")
                        .font(.system(size: 30, weight: .bold))
                        .multilineTextAlignment(.center)
                    
                    Text("Simple, secure, and fully offline storage for your most private data.")
                        .font(.system(size: 17, weight: .medium))
                        .foregroundStyle(.secondary)
                        .multilineTextAlignment(.center)
                        .padding(.horizontal)
                }
                
                // App Store button
                Link(destination: URL(string: "https://apps.apple.com/us/app/private-vault-offline-safe/id6762105214")!) {
                    HStack {
                        Image(systemName: "arrow.down.circle.fill")
                        Text("Download on the App Store")
                            .fontWeight(.semibold)
                    }
                    .font(.system(size: 17))
                    .foregroundColor(.white)
                    .padding(.horizontal, 22)
                    .padding(.vertical, 14)
                    .background(
                        RoundedRectangle(cornerRadius: 16, style: .continuous)
                            .fill(Color.black)
                    )
                }
                
                // Overview
                IntroCard(title: "Overview") {
                    Text("""
Private Vault is a simple yet powerful secure storage app designed to keep your most sensitive data truly private — directly on your device.

No cloud. No account. No tracking. Ever.
""")
                }
                
                // Screenshots
                VStack(alignment: .leading, spacing: 14) {
                    Text("App Preview")
                        .font(.title2.bold())
                        .frame(maxWidth: .infinity, alignment: .leading)
                    
                    IntroScreenshot(imageName: "anh1")
                    IntroScreenshot(imageName: "anh2")
                    IntroScreenshot(imageName: "anh3")
                }
                .padding(.horizontal)
                
                // Features
                IntroCard(title: "Secure by Design") {
                    BulletText("Protect your vault with a PIN and optional Face ID.")
                    BulletText("Automatically locks when the app goes to background.")
                }
                
                IntroCard(title: "Store What Matters") {
                    BulletText("Private notes")
                    BulletText("Images from Photos or Camera")
                    BulletText("Passwords with quick copy")
                    BulletText("Add, edit, delete, and search instantly")
                }
                
                IntroCard(title: "Your Data") {
                    Text("Everything stays on your device — 100% offline.")
                }
                
                IntroCard(title: "Smart Protection Features") {
                    BulletText("Decoy Vault: Use a secondary PIN to open a fake vault")
                    BulletText("Disguise Mode: Change the app icon to a calculator")
                }
                
                IntroCard(title: "Multi-language Support") {
                    BulletText("English")
                    BulletText("Spanish")
                    BulletText("Portuguese")
                    BulletText("Simplified Chinese")
                }
                
                IntroCard(title: "Why Private Vault") {
                    Text("""
Private Vault is built for speed, simplicity, and absolute privacy.
It gives users a clean and reliable place to store sensitive information without cloud sync, tracking, or unnecessary complexity.
""")
                }
                
                Spacer(minLength: 30)
            }
            .padding(.horizontal)
        }
        .background(Color(.systemGroupedBackground))
        .navigationTitle("Private Vault")
        .navigationBarTitleDisplayMode(.inline)
    }
}

struct IntroCard<Content: View>: View {
    let title: String
    @ViewBuilder let content: Content
    
    var body: some View {
        VStack(alignment: .leading, spacing: 14) {
            Text(title)
                .font(.title3.bold())
            
            content
                .font(.body)
                .foregroundStyle(.primary)
        }
        .frame(maxWidth: .infinity, alignment: .leading)
        .padding(20)
        .background(
            RoundedRectangle(cornerRadius: 22, style: .continuous)
                .fill(Color(.secondarySystemBackground))
        )
    }
}

struct BulletText: View {
    let text: String
    
    init(_ text: String) {
        self.text = text
    }
    
    var body: some View {
        HStack(alignment: .top, spacing: 10) {
            Text("•")
                .font(.body.bold())
            Text(text)
                .frame(maxWidth: .infinity, alignment: .leading)
        }
    }
}

struct IntroScreenshot: View {
    let imageName: String
    
    var body: some View {
        Image(imageName)
            .resizable()
            .scaledToFit()
            .frame(maxWidth: .infinity)
            .clipShape(RoundedRectangle(cornerRadius: 24, style: .continuous))
            .shadow(color: .black.opacity(0.12), radius: 10, x: 0, y: 6)
    }
}

#Preview {
    NavigationStack {
        PrivateVaultIntroView()
    }
}
