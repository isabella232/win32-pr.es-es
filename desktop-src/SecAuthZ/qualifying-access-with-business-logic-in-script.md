---
description: Uso de scripts de reglas de negocios en script para proporcionar lógica en tiempo de ejecución para comprobar el acceso.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Calificar el acceso con lógica de negocios en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b77ff1d6d520780d30efab5619c3e9bc3c896ad88315fba56e3a19e05d3ae97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907555"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Calificar el acceso con lógica de negocios en el script

Use scripts de reglas de negocios para proporcionar lógica en tiempo de ejecución para comprobar el acceso. Para obtener más información sobre las reglas de negocios, [vea Business Rules](business-rules.md).

Para asignar una regla de negocio a una tarea, establezca primero la propiedad [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) del objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa la tarea. El script debe escribirse mediante el lenguaje de programación Visual Basic Scripting Edition (VBScript) o JScript software de desarrollo. Después de especificar el lenguaje de script, establezca la propiedad [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) del objeto **IAzTask** con una representación de cadena del script.

Al comprobar el acceso de una operación contenida en una tarea que tiene una regla de negocios asociada, la aplicación debe crear dos matrices del mismo tamaño que los parámetros *varParameterNames* y *varParameterValues* del método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un objeto [**IAzClientContext.**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) Para obtener información sobre cómo crear un contexto de cliente, vea [Establecer un contexto de cliente en el script](establishing-a-client-context-in-script.md).

El [**método AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crea un [**objeto AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que se pasa al script de regla de negocios. A continuación, el script [**establece la propiedad BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) del **objeto AzBizRuleContext.** Un valor true **indica** que se concede acceso y un valor **false** indica que se deniega el acceso.

No se puede asignar un script de regla de negocios a un [**objeto IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenido en un objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegado.

En el ejemplo siguiente se muestra cómo usar un script de regla de negocios para comprobar el acceso de un cliente a una operación. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada Expense, una tarea denominada Submit Expense y una operación denominada UseFormControl.


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



