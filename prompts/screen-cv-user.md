JOB
Title: {{ $json.job_title }}
Company: {{ $json.company }}
About the role: {{ $json.job_summary }}
Minimum years: {{ $json.min_years }}
Location rule: {{ $json.location_rule }}

MUST HAVE (evaluate every line, in this order)
{{ $json.must_haves }}

NICE TO HAVE
{{ $json.nice_to_haves }}

CANDIDATE (from the application)
Name: {{ $json.name }}
Email: {{ $json.email }}
Stated location: {{ $json.location }}
Note: {{ $json.note }}

CV TEXT
{{ $json.cv_text }}

SCORING RULES
skills_score (0-100): coverage of the must-have and nice-to-have skills with evidence of real use. All must-have skills with production evidence = 70+. Each nice-to-have adds a little.
experience_score (0-100): relevant years and seniority vs the minimum. Exactly the minimum = 60. 2+ years above with ownership or leadership = 85+. Below the minimum = under 50.
location_score (0-100): inside the allowed time zones = 100. Outside but the CV or note says they will work UK hours = 60. Outside with no signal = 20. Unknown = 50.
must_haves: one entry per must-have line, met true or false, with a short evidence quote or "not mentioned".
years_experience: total professional years in relevant roles, from the dates in the CV. Use {{ $now.year }} for "present".
red_flags: only real ones (unexplained gaps over 6 months, many jobs under 1 year, dates that do not add up). Empty array if none.
