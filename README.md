# Quiz-Clean-Code-2-c.22-l.1-
Clean
Define

    Select all nondescriptive and misspelled column headers (ApplicationP, AboutC, RequiredQual, JobRequirment) and replace them with full words (ApplicationProcedure, AboutCompany, RequiredQualifications, JobRequirement)
    Select all records in the StartDate column that have "As soon as possible", "Immediately", etc. and replace the text in those cells with "ASAP"

Code

df_clean = df.copy()

    Select all nondescriptive and misspelled column headers (ApplicationP, AboutC, RequiredQual, JobRequirment) and replace them with full words (ApplicationProcedure, AboutCompany, RequiredQualifications, JobRequirement)

df_clean = df_clean.rename(columns={'ApplicationP': 'ApplicationProcedure',

                                    'AboutC': 'AboutCompany',

                                    'RequiredQual': 'RequiredQualifications',

                                    'JobRequirment': 'JobRequirements'})

    Select all records in the StartDate column that have "As soon as possible", "Immediately", etc. and replace the text in those cells with "ASAP"

asap_list = ['Immediately', 'As soon as possible', 'Upon hiring',

             'Immediate', 'Immediate employment', 'As soon as possible.', 'Immediate job opportunity',

             '"Immediate employment, after passing the interview."',

             'ASAP preferred', 'Employment contract signature date',

             'Immediate employment opportunity', 'Immidiately', 'ASA',

             'Asap', '"The position is open immediately but has a flexible start date depending on the candidates earliest availability."',

             'Immediately upon agreement', '20 November 2014 or ASAP',

             'immediately', 'Immediatelly',

             '"Immediately upon selection or no later than November 15, 2009."',

             'Immediate job opening', 'Immediate hiring', 'Upon selection',

             'As soon as practical', 'Immadiate', 'As soon as posible',

             'Immediately with 2 months probation period',

             '12 November 2012 or ASAP', 'Immediate employment after passing the interview',

             'Immediately/ upon agreement', '01 September 2014 or ASAP',

             'Immediately or as per agreement', 'as soon as possible',

             'As soon as Possible', 'in the nearest future', 'immediate',

             '01 April 2014 or ASAP', 'Immidiatly', 'Urgent',

             'Immediate or earliest possible', 'Immediate hire',

             'Earliest  possible', 'ASAP with 3 months probation period.',

             'Immediate employment opportunity.', 'Immediate employment.',

             'Immidietly', 'Imminent', 'September 2014 or ASAP', 'Imediately']

​

for

    df_clean.StartDate.replace( , , inplace=True)
