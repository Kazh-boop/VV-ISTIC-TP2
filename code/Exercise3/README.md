# Code of your exercise

```xml
<?xml version="1.0"?>

<ruleset name="MyCustomRules" xmlns="http://pmd.sourceforge.net/ruleset/2.0.0"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://pmd.sourceforge.net/ruleset/2.0.0 http://pmd.sourceforge.net/ruleset_2_0_0.xsd">

    <description>
        Custom rules for preventing complex code.
    </description>

    <rule name="AvoidDeeplyNestedIfStatements"
          language="java"
          message="Avoid three or more nested if statements"
          class="net.sourceforge.pmd.lang.rule.XPathRule">

        <description>
            Detects the use of three or more nested if statements in Java code.
        </description>

        <priority>3</priority>

        <properties>
            <property name="xpath">
                <value>
                    <![CDATA[
                    //IfStatement[count(.//IfStatement) >= 3]
                    ]]>
                </value>
            </property>
        </properties>
    </rule>
</ruleset>
```