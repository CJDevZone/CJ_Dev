<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>C# Code with Red Color</title>
    <style>
        pre {
            color: red;
        }
    </style>
</head>
<body>
    <pre>
        <code>
using System;
using System.Windows.Forms;

namespace SkillBarExample
{
    public partial class MainForm : Form
    {
        public MainForm() => InitializeComponent();

        private void MainForm_Load(object sender, EventArgs e) => SetSkillLevel(90);

        private void SetSkillLevel(int skillLevel)
        {
            skillLevel = Math.Max(0, Math.Min(100, skillLevel));
            panelFilled.Width = (int)(panelSkillBar.Width * skillLevel / 100.0);
            labelSkillLevel.Text = $"{skillLevel}%";
        }
    }
}
        </code>
    </pre>
</body>
</html>
