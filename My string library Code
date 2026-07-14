#pragma once

#include <iostream>
#include <vector>

using namespace std;

class ClsString
{
private:

	string _Value;
public:

	ClsString()
	{
		_Value = "";
	}

	ClsString(string Value)
	{
		_Value = Value;
	}

	void SetValue(string Value)
	{
		_Value = Value;
	}

	string GetValue()
	{
		return _Value;
	}

	__declspec(property(get = GetValue, put = SetValue)) string Value;

	static short CountWords(string S1)
	{
		string delim = " ";
		short Counter = 0;
		short pos = 0;
		string sWord;

		while ((pos = S1.find(delim)) != std::string::npos)
		{
			sWord = S1.substr(0, pos);
			if (sWord != "")
			{
				Counter++;
			}
			S1.erase(0, pos + delim.length());
		}

		if (S1 != "")
		{
			Counter++;
		}
		return Counter;
	}

	short CountWords()
	{
		return CountWords(_Value);
	};

	static vector<string> SplitString(string Text, string delim = "#//#")
	{
		vector<string> vString;

		short pos = 0;
		string word;

		while ((pos = Text.find(delim)) != string::npos)
		{
			word = Text.substr(0, pos);
			if (word != "")
			{
				vString.push_back(word);
			}
			Text.erase(0, pos + delim.size());
		}
		if (Text != "")
			vString.push_back(Text);

		return vString;
	}

	vector<string> SplitString()
	{
		return SplitString(_Value," ");
	}

	static void PrintFirstLetterOfEveryWord(string Text)
	{
		bool IsFirstLetter = true;

		cout << "First letters of this string : \n";


		for (int i = 0; i < Text.size(); i++)
		{
			if (Text[i] != ' ' && IsFirstLetter)
			{
				cout << Text[i] << "\n";
			}
			IsFirstLetter = (Text[i] == ' ' ? true : false);
		}
	}

	void PrintFirstLetterOfEveryWord()
	{
		PrintFirstLetterOfEveryWord(_Value);
	}

	static string MakeFirstLetterCaptalOfString(string Text)
	{
		bool IsFirstLetter = true;

		for (int i = 0; i < Text.size(); i++)
		{
			if (Text[i] != ' ' && IsFirstLetter)
			{
				Text[i] = toupper(Text[i]);
			}

			IsFirstLetter = (Text[i] == ' ' ? true : false);
		}
		return Text;
	}

	string MakeFirstLetterCaptalOfString()
	{
		return MakeFirstLetterCaptalOfString(_Value);
	}

	static string MakeFirstLetterSmalOfString(string Text)
	{
		bool IsFirstLetter = true;

		for (int i = 0; i < Text.size(); i++)
		{
			if (Text[i] != ' ' && IsFirstLetter)
			{
				Text[i] = tolower(Text[i]);
			}

			IsFirstLetter = (Text[i] == ' ' ? true : false);
		}
		return Text;
	}

	string MakeFirstLetterSmalOfString()
	{
		return MakeFirstLetterSmalOfString(_Value);
	}

	static string MakeStringSmall(string Text)
	{
		for (int i = 0; i < Text.size(); i++)
		{
			Text[i] = tolower(Text[i]);
		}
		return Text;
	}

	string MakeStringSmall()
	{
		return MakeStringSmall(_Value);
	}

	static string MakeStringCaptal(string Text)
	{
		for (int i = 0; i < Text.size(); i++)
		{
			Text[i] = toupper(Text[i]);
		}
		return Text;
	}

	string MakeStringCaptal()
	{
		return MakeStringCaptal(_Value);
	}

	static char InvertCharCase(char Text)
	{
		return(isupper(Text) ? tolower(Text) : toupper(Text));
	}

	static string InvertAllStringCase(string Text)
	{
		for (int i = 0; i < Text.size(); i++)
		{
			Text[i] = InvertCharCase(Text[i]);
		}
		return Text;
	}

	string InvertAllStringCase()
	{
		return InvertAllStringCase(_Value);
	}

	static int CountCapitalLetters(string Text)
	{
		int CapitalLetters = 0;

		for (int i = 0; i < Text.size(); i++)
		{
			if (isupper(Text[i]))
				CapitalLetters++;
		}
		return CapitalLetters;
	}

	int CountCapitalLetters()
	{
		return CountCapitalLetters(_Value);
	}

	static int CountSmallLetters(string Text)
	{
		int SmallLetters = 0;

		for (int i = 0; i < Text.size(); i++)
		{
			if (islower(Text[i]))
				SmallLetters++;
		}
		return SmallLetters;
	}

	int CountSmallLetters()
	{
		return CountSmallLetters(_Value);
	}

	static short CountCharInString(string Text, char Char)
	{
		short Counter = 0;

		for (short i = 0; i < Text.size(); i++)
		{
			if (Text[i] == Char)
				Counter++;
		}
		return Counter;
	}

	short CountCharInString(char Char)
	{
		return CountCharInString(_Value, Char);
	}

	static short CountLetter(string Text, char Char, bool MatchCase = true)
	{
		short Counter = 0;

		for (short i = 0; i < Text.size(); i++)
		{
			if (MatchCase)
			{
				if (Text[i] == Char)
					Counter++;
			}
			else
			{
				if (toupper(Char) == toupper(Text[i]))
					Counter++;
			}
		}

		return Counter;
	}

	short CountLetter(char Char, bool MatchCase = true)
	{
		return CountLetter(_Value, Char, MatchCase);
	}

	static bool CheckVowelLetter(char Letter)
	{
		Letter = tolower(Letter);
		return (Letter == 'a' || Letter == 'e' || Letter == 'i' || Letter == 'o' || Letter == 'u');
	}

	static short CountVowelLetters(string Text)
	{
		short Counter = 0;

		for (int i = 0; i < Text.size(); i++)
		{
			if (CheckVowelLetter(Text[i]))
				Counter++;
		}

		return Counter;
	}

	short CountVowelLetters()
	{
		return CountVowelLetters(_Value);
	}

	static void PrintVowelLetters(string Text)
	{
		cout << "\nVowel letters : ";

		for (int i = 0; i < Text.size(); i++)
		{
			if (CheckVowelLetter(Text[i]))
				cout << Text[i] << "  ";
		}
	}

	void PrintVowelLetters()
	{
		PrintVowelLetters(_Value);
	}

	static void PrintEachWord(string Text)
	{
		string delim = " ";

		cout << "\nWords : \n\n";
		short pos = 0;
		string word;

		while ((pos = Text.find(delim)) != std::string::npos)
		{
			word = Text.substr(0, pos);
			if (word != "")
			{
				cout << word << "\n";
			}
			Text.erase(0, pos + delim.size());
		}
		if (Text != "")
			cout << Text << endl;
	}

	void PrintEachWord()
	{
		PrintEachWord(_Value);
	}

	static string TrimRight(string Text)
	{
		for (int i = Text.size() - 1; i >= 0; i--)
		{
			if (Text[i] != ' ')
				return Text.substr(0, i + 1);
		}

		return Text;
	}

	string TrimRight()
	{
		return TrimRight(_Value);
	}

	static string TrimLeft(string Text)
	{
		for (int i = 0; i < Text.size(); i++)
		{
			if (Text[i] != ' ')
				return Text.substr(i, Text.size() - 1);
		}

		return Text;
	}

	string TrimLeft()
	{
		return TrimLeft(_Value);
	}

	static string Trim(string Text)
	{
		return TrimRight(TrimLeft(Text));
	}

	string Trim()
	{
		return Trim(_Value);
	}

	static string JoinString(vector<string> vString, string delim = " ")
	{
		string S;

		for (string& i : vString)
		{
			S += i + delim;
		}

		return S.substr(0, S.size() - delim.size());
	}

	static string ReverseString(string Text, string delim = " ")
	{
		vector<string> vString = SplitString(Text);
		vector<string>::iterator iter = vString.end();

		string S1 = "";

		while (iter != vString.begin())
		{
			iter--;
			S1 += *iter + delim;
		}

		return S1.substr(0, S1.size() - 1);
	}

	string ReverseString()
	{
		return ReverseString(_Value);
	}

	static string ReplaceWordsInString(string Text, string Word, string WordToReplace)
	{
		short pos = Text.find(Word);

		while (pos != string::npos)
		{
			Text = Text.replace(pos, Word.length(), WordToReplace);
			pos = Text.find(Word);
		}

		return Text;
	}

	string ReplaceWordsInString(string Word, string WordToReplace)
	{
		return ReplaceWordsInString(_Value, Word, WordToReplace);
	}

	static string RemovePunctInString(string Text)
	{
		string S1 = "";

		for (short i = 0; i < Text.size(); i++)
		{
			if (!ispunct(Text[i]))
				S1 += Text[i];
		}

		return S1;
	}

	string RemovePunctInString()
	{
		return RemovePunctInString(_Value);
	}
};
