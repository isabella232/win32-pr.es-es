---
description: 'Llame al método IAzClientContext:: AccessCheck para comprobar si el cliente tiene acceso a una o varias operaciones.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Comprobando el acceso del cliente a los recursos solicitados en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667731"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="f3c32-103">Comprobando el acceso del cliente a los recursos solicitados en el script</span><span class="sxs-lookup"><span data-stu-id="f3c32-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="f3c32-104">Llame al método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para comprobar si el cliente tiene acceso a una o varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="f3c32-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="f3c32-105">Para obtener información sobre cómo crear un objeto **IAzClientContext** , vea [establecer un contexto de cliente en un script](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="f3c32-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="f3c32-106">Un cliente puede ser miembro de más de un rol, y una operación se puede asignar a más de una tarea, por lo que el administrador de autorización comprueba todos los roles y las tareas.</span><span class="sxs-lookup"><span data-stu-id="f3c32-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="f3c32-107">Si un rol al que pertenece el cliente contiene cualquier tarea que contenga una operación, se concede el acceso a esa operación.</span><span class="sxs-lookup"><span data-stu-id="f3c32-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="f3c32-108">Para comprobar el acceso solo a un rol al que pertenece el cliente, establezca la propiedad [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) del objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="f3c32-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="f3c32-109">Al inicializar el almacén de directivas de autorización para la comprobación de acceso, debe pasar cero como el valor del parámetro *lFlags* del método [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) del objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="f3c32-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="f3c32-110">También es posible aplicar la lógica de negocios en tiempo de ejecución para calificar el acceso.</span><span class="sxs-lookup"><span data-stu-id="f3c32-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="f3c32-111">Para obtener información sobre cómo calificar el acceso con la lógica de negocios, consulte [acceso de calificación con lógica de negocios en script](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="f3c32-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="f3c32-112">En el ejemplo siguiente se muestra cómo comprobar el acceso de un cliente a una operación.</span><span class="sxs-lookup"><span data-stu-id="f3c32-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="f3c32-113">En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada///Expense y una operación denominada UseFormControl.</span><span class="sxs-lookup"><span data-stu-id="f3c32-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


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

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



