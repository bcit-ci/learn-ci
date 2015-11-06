XML Examples

The original data for the North American Sales example is in NA-SALES-Q1-Q4_2010_eng.pdf.

The stand-alone XML documents to model this, without constraints, are the sales04-*.xml ones.

The DTD-constrained documents, and their corresponding DTDs, are the sales05*.* ones.

The examples model the same data, but from six different perspectives...
- elements: an element-centric approach, following the data source order, with the only attribute being the quarter (column) of a sales figure
- embedded: nested by source, with country and vehicle category abbreviations embedded
- quarter: nester by quarter, i.e. vehicles sold, by vehicle type, by country, by quarter
- source: nested per the order of the data source, i.e. quarterly sales, within vehicle type, within country
- table: no nesting, more like a spreadsheet perspective
- vehicle: nested by vehicle type, i.e. quarterly sales, within country, within vehicle type

The *source* perspective is natural, but not necessarily ideal.
The *vehicle* perspective is similar.
The *elements* perspective shows a different way of modeling - easier to program, perhaps, but not ideal.
The *table* perspective is there to show you that it can be done - intuitive to an RDB type, perhaps, but not ideal. I can't think of anyone who would use this.
The *quarter* perspective is also there to show you that it can be done. It ends up wordy, but conceptually easy because all you have to do to add updated sales data is add an additional "quarter" element. This made sense to one student, who had trouble figuring out the structure; this was a solution for him. I can't think of anyone who would use this, either.
The *embedded* perspective is the one that makes the most sense for modeling data in XML. It offers the possibility of rich constraints for country and vehicle categories, though not with a DTD. It exploits the rich structure that XML affords, compared to an RDB. It is the perspective that I would use.

