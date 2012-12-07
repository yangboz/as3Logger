as3Logger
=========

Flex's ILogger adapter to the pure AS3 project.

Usage
=========


Use a simple utility(com.godpaper.as3.utils.LogUtil) method to retrieve the logger for a particular class, instead of passing in the qualified class name as a string. just like:(Declare Loggers as Static Constants)
 * private static const LOG:ILogger = LogUtil.getLogger(MyClass);

Format Log Statements Consistently:
* LOG.error("Something bad has happened: event={0}, message={1}", event.type, message);
 
Parameterize Log Statements:
* LOG.error("Something bad has happened: event={0}, message={1}", event.type, message);

Use Log Levels to Indicate Severity:
* LOG.error("The service has failed and no data is available.");

Use Log Filters for Focus:
* target.filters = [ "my.important.package.MyClass" ];
* target.level = LogEventLevel.INFO;

Include Categories to Show Class Names:
* target.includeCategory = true;

More configurations:
=========

	 * target.includeLevel=LoggerConfig.includeLevel;
     * target.includeDate=LoggerConfig.includeDate;
	 * target.includeCategory=LoggerConfig.includeCategory;
	 * target.includeTime=LoggerConfig.includeTime;
	 * target.includeMemory=LoggerConfig.includeMemory;
	 * target.fieldSeparator=LoggerConfig.fieldSeparator;
	 * target.filters=LoggerConfig.filters;
	 * target.level=LoggerConfig.level;
	 
Example
=========

11:32:24.222->[DEBUG]->[34.352M]->ApplicationBase->applicationCompleteHandler@onContextCreated,driverInfo(software) is:true
