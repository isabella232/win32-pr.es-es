---
description: Usar scripts de reglas de negocios en script para proporcionar lógica de tiempo de ejecución para comprobar el acceso.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Acceso de calificación con lógica de negocios en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666667"
---
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="cc858-103">Acceso de calificación con lógica de negocios en script</span><span class="sxs-lookup"><span data-stu-id="cc858-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="cc858-104">Use scripts de reglas de negocios para proporcionar lógica de tiempo de ejecución para comprobar el acceso.</span><span class="sxs-lookup"><span data-stu-id="cc858-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="cc858-105">Para obtener más información acerca de las reglas de negocios, consulte [reglas de negocios](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="cc858-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="cc858-106">Para asignar una regla de negocios a una tarea, establezca primero la propiedad [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) del objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) que representa la tarea.</span><span class="sxs-lookup"><span data-stu-id="cc858-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="cc858-107">El script se debe escribir con el lenguaje de programación de Visual Basic Scripting Edition (VBScript) o el software de desarrollo de JScript.</span><span class="sxs-lookup"><span data-stu-id="cc858-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="cc858-108">Después de especificar el lenguaje de script, establezca la propiedad [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) del objeto **IAzTask** con una representación de cadena del script.</span><span class="sxs-lookup"><span data-stu-id="cc858-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="cc858-109">Cuando se comprueba el acceso para una operación incluida en una tarea que tiene una regla de negocios asociada, la aplicación debe crear dos matrices del mismo tamaño que se van a pasar como los parámetros *varParameterNames* y *VarParameterValues* del método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="cc858-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="cc858-110">Para obtener información sobre cómo crear un contexto de cliente, consulte [establecer un contexto de cliente en un script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="cc858-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="cc858-111">El método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crea un objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que se pasa al script de regla de negocios.</span><span class="sxs-lookup"><span data-stu-id="cc858-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="cc858-112">Después, el script establece la propiedad [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) del objeto **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="cc858-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="cc858-113">Un valor de **true** indica que se concede el acceso y un valor de **false** indica que se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="cc858-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="cc858-114">Un script de regla de negocios no se puede asignar a un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenido por un objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegado.</span><span class="sxs-lookup"><span data-stu-id="cc858-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="cc858-115">En el ejemplo siguiente se muestra cómo usar un script de regla de negocios para comprobar el acceso de un cliente a una operación.</span><span class="sxs-lookup"><span data-stu-id="cc858-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="cc858-116">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada///Expense, una tarea denominada Submit Expense y una operación denominada UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="cc858-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



