import { Sprout, MessageCircle, Camera, Mic, Phone, Users } from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card } from "@/components/ui/card";
import ChatInterface from "@/components/ChatInterface";
import QuickActions from "@/components/QuickActions";
import LanguageSelector from "@/components/LanguageSelector";
import heroImage from "@/assets/hero-farmer.jpg";

const Index = () => {
  return (
    <div className="min-h-screen bg-background">
      {/* Header */}
      <header className="sticky top-0 z-50 w-full border-b border-border bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60">
        <div className="container flex h-16 items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="p-2 rounded-lg bg-gradient-primary text-primary-foreground">
              <Sprout className="h-6 w-6" />
            </div>
            <div>
              <h1 className="text-xl font-bold">KrishiBot</h1>
              <p className="text-xs text-muted-foreground">കൃഷിബോട്ട്</p>
            </div>
          </div>
          <LanguageSelector />
        </div>
      </header>

      {/* Hero Section */}
      <section className="relative py-20 overflow-hidden">
        <div 
          className="absolute inset-0 bg-cover bg-center bg-no-repeat opacity-20"
          style={{ backgroundImage: `url(${heroImage})` }}
        />
        <div className="absolute inset-0 bg-gradient-hero opacity-10" />
        
        <div className="relative container mx-auto px-4 text-center">
          <h2 className="text-4xl md:text-6xl font-bold mb-6 bg-gradient-hero bg-clip-text text-transparent">
            Your AI Farming Assistant
          </h2>
          <p className="text-xl md:text-2xl text-muted-foreground mb-4">
            നിങ്ങളുടെ AI കൃഷി സഹായി
          </p>
          <p className="text-lg text-muted-foreground mb-8 max-w-2xl mx-auto">
            Get instant, expert advice on crops, pests, weather, and market prices in your local language. 24/7 support for farmers.
          </p>
          
          <div className="flex flex-col sm:flex-row gap-4 justify-center mb-12">
            <Button className="bg-gradient-primary hover:shadow-glow transition-smooth text-lg px-8 py-3">
              <MessageCircle className="mr-2 h-5 w-5" />
              Start Chatting
            </Button>
            <Button variant="outline" className="text-lg px-8 py-3 hover:bg-accent hover:text-accent-foreground transition-smooth">
              <Phone className="mr-2 h-5 w-5" />
              Call Expert
            </Button>
          </div>

          {/* Features */}
          <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mb-16">
            <Card className="p-6 bg-gradient-card shadow-soft">
              <div className="p-3 rounded-full bg-gradient-primary text-primary-foreground w-fit mx-auto mb-4">
                <MessageCircle className="h-6 w-6" />
              </div>
              <h3 className="font-semibold mb-2">Voice & Text Chat</h3>
              <p className="text-muted-foreground text-sm">Ask questions in Malayalam, Hindi, or English using voice or text</p>
            </Card>
            
            <Card className="p-6 bg-gradient-card shadow-soft">
              <div className="p-3 rounded-full bg-gradient-secondary text-secondary-foreground w-fit mx-auto mb-4">
                <Camera className="h-6 w-6" />
              </div>
              <h3 className="font-semibold mb-2">Image Recognition</h3>
              <p className="text-muted-foreground text-sm">Upload crop photos for instant disease and pest identification</p>
            </Card>
            
            <Card className="p-6 bg-gradient-card shadow-soft">
              <div className="p-3 rounded-full bg-gradient-primary text-primary-foreground w-fit mx-auto mb-4">
                <Users className="h-6 w-6" />
              </div>
              <h3 className="font-semibold mb-2">Expert Support</h3>
              <p className="text-muted-foreground text-sm">Connect with agriculture officers when you need human expertise</p>
            </Card>
          </div>
        </div>
      </section>

      {/* Quick Actions */}
      <section className="py-16 bg-muted/30">
        <div className="container mx-auto px-4">
          <h3 className="text-3xl font-bold text-center mb-2">Quick Help</h3>
          <p className="text-muted-foreground text-center mb-12">Choose what you need help with</p>
          <QuickActions />
        </div>
      </section>

      {/* Chat Interface */}
      <section className="py-16">
        <div className="container mx-auto px-4">
          <h3 className="text-3xl font-bold text-center mb-2">Try KrishiBot Now</h3>
          <p className="text-muted-foreground text-center mb-12">Start a conversation and get instant farming advice</p>
          <ChatInterface />
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-card border-t border-border py-12">
        <div className="container mx-auto px-4 text-center">
          <div className="flex items-center justify-center gap-2 mb-4">
            <div className="p-2 rounded-lg bg-gradient-primary text-primary-foreground">
              <Sprout className="h-5 w-5" />
            </div>
            <span className="font-bold text-lg">KrishiBot</span>
          </div>
          <p className="text-muted-foreground mb-4">
            Empowering farmers with AI-powered agricultural guidance
          </p>
          <p className="text-sm text-muted-foreground">
            © 2024 KrishiBot. Supporting farmers across India.
          </p>
        </div>
      </footer>
    </div>
  );
};

export default Index;
