# prosper Loan Data Exploration

## Investigation Overview


>The primary goal of this analysis is to develop a comprehensive understanding of the key factors driving the dynamics within the loan portfolio. Specifically, we aim to explore the relationships between the core loan variables, including Loan Original Amount, LP_CustomerPrincipalPayments, MonthlyLoanPayment, Debt-to-Income Ratio, Stated Monthly Income, Employment Status, and Income Range.


## Dataset Overview

>The loan dataset includes information on customers with varying loan repayment statuses. It contains data on customers who have fully paid off their loans, those who have been delinquent and sent to collections without completing repayment, as well as customers who have only paid off their loans after being sent to collections. The original dataset had 113,937 rows and 81 columns

## Summary of Findings

>The exploration of the loan dataset revealed several key insights. There is a strong positive relationship between the loan original amount and the monthly loan payment, with the relationship becoming more linear when both variables are transformed. The distribution of the "Income Verifiability" feature a larger proportion of loans have verifiable income compared to non-verifiable income. The pairwise scatter plot matrix unveiled complex relationships and interactions between various loan variables, such as Debt-to-Income Ratio, Stated Monthly Income, and Loan Original Amount, which may play a role in influencing loan outcomes and should be further investigated. Finally, the insights gained from this initial analysis suggest the need for a more comprehensive analysis, including the development of predictive models, to yield valuable insights into the drivers of loan repayment status and other critical outcomes, as the complex relationships and interactions observed in the data may hold the key to understanding loan performance and outcomes.

## Key Insights for Presentation
>For the presentation, I focused on the influence of the key loan variables. 

>I start by, introducing each key loan variable one by one. Afterward, I use the count plots of loan Verifiability. I'm only looking at this relationship here since by understanding the distribution of income verifiability, you can make more informed decisions. The other key loan variables, such as Customer Principal Payments, Debt-to-Income Ratio, and Stated Monthly Income, are covered afterward, using facet plots and the correlation matrix.


```python
!jupyter nbconvert --template "pythoncodeblocks.tpl" --to markdown README.ipynb
```

    Traceback (most recent call last):
      File "/opt/venv/lib/python3.10/site-packages/traitlets/traitlets.py", line 632, in get
        value = obj._trait_values[self.name]
    KeyError: 'template_paths'
    
    During handling of the above exception, another exception occurred:
    
    Traceback (most recent call last):
      File "/opt/venv/bin/jupyter-nbconvert", line 8, in <module>
        sys.exit(main())
      File "/opt/venv/lib/python3.10/site-packages/jupyter_core/application.py", line 283, in launch_instance
        super().launch_instance(argv=argv, **kwargs)
      File "/opt/venv/lib/python3.10/site-packages/traitlets/config/application.py", line 1075, in launch_instance
        app.start()
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/nbconvertapp.py", line 420, in start
        self.convert_notebooks()
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/nbconvertapp.py", line 586, in convert_notebooks
        self.exporter = cls(config=self.config)
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/templateexporter.py", line 350, in __init__
        super().__init__(config=config, **kw)
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/exporter.py", line 123, in __init__
        self._init_preprocessors()
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/templateexporter.py", line 535, in _init_preprocessors
        conf = self._get_conf()
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/templateexporter.py", line 553, in _get_conf
        for path in map(Path, self.template_paths):
      File "/opt/venv/lib/python3.10/site-packages/traitlets/traitlets.py", line 687, in __get__
        return t.cast(G, self.get(obj, cls))  # the G should encode the Optional
      File "/opt/venv/lib/python3.10/site-packages/traitlets/traitlets.py", line 635, in get
        default = obj.trait_defaults(self.name)
      File "/opt/venv/lib/python3.10/site-packages/traitlets/traitlets.py", line 1897, in trait_defaults
        return t.cast(Sentinel, self._get_trait_default_generator(names[0])(self))
      File "/opt/venv/lib/python3.10/site-packages/traitlets/traitlets.py", line 1241, in __call__
        return self.func(*args, **kwargs)
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/templateexporter.py", line 564, in _template_paths
        template_names = self.get_template_names()
      File "/opt/venv/lib/python3.10/site-packages/nbconvert/exporters/templateexporter.py", line 652, in get_template_names
        raise ValueError(msg)
    ValueError: No template sub-directory with name 'pythoncodeblocks.tpl' found in the following paths:
    	/home/student/.local/share/jupyter
    	/opt/venv/share/jupyter
    	/usr/local/share/jupyter
    	/usr/share/jupyter

