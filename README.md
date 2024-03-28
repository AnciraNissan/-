# -
情感音乐利用情感识别技术和音乐心理学,根据用户的情绪状态智能推荐音乐,并引导用户通过音乐达到情绪管理和心理健康的目的。
import random

# Simulated Emotion Recognition Function
def recognize_emotion(user_input):
    """
    Simulates emotion recognition from user input.
    In a real application, this might involve analyzing voice tone, facial expressions, or text input using AI.
    
    For demo purposes, we'll assume the function can detect the following emotions: Happy, Sad, Angry, Relaxed.
    """
    emotions = ["Happy", "Sad", "Angry", "Relaxed"]
    return random.choice(emotions)

# Music Recommendation System
def recommend_music(emotion):
    """
    Recommends music based on the recognized emotion.
    """
    music_library = {
        "Happy": ["Happy Tune - Artist A", "Joyful Melody - Artist B"],
        "Sad": ["Melancholy Blues - Artist C", "Rainy Day Reflection - Artist D"],
        "Angry": ["Fury Unleashed - Artist E", "Rage Against the Night - Artist F"],
        "Relaxed": ["Calm Seas - Artist G", "Meditative State - Artist H"]
    }
    
    recommendations = music_library.get(emotion, [])
    return recommendations

# Main Function to Simulate the Application Flow
def main():
    print("Welcome to Emotional Music: A Music Therapy Application")
    user_input = input("Tell me about your day or how you're feeling: ")
    
    detected_emotion = recognize_emotion(user_input)
    print(f"\nDetected Emotion: {detected_emotion}")
    
    music_recommendations = recommend_music(detected_emotion)
    if music_recommendations:
        print("\nBased on your emotion, we recommend the following tracks:")
        for track in music_recommendations:
            print(f"- {track}")
    else:
        print("\nSorry, we couldn't find a music recommendation for your mood.")

if __name__ == "__main__":
    main()
