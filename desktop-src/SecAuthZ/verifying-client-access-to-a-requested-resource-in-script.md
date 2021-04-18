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
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Comprobando el acceso del cliente a los recursos solicitados en el script

Llame al método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para comprobar si el cliente tiene acceso a una o varias operaciones. Para obtener información sobre cómo crear un objeto **IAzClientContext** , vea [establecer un contexto de cliente en un script](establishing-a-client-context-in-script.md).

Un cliente puede ser miembro de más de un rol, y una operación se puede asignar a más de una tarea, por lo que el administrador de autorización comprueba todos los roles y las tareas. Si un rol al que pertenece el cliente contiene cualquier tarea que contenga una operación, se concede el acceso a esa operación.

Para comprobar el acceso solo a un rol al que pertenece el cliente, establezca la propiedad [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) del objeto [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .

Al inicializar el almacén de directivas de autorización para la comprobación de acceso, debe pasar cero como el valor del parámetro *lFlags* del método [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) del objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .

También es posible aplicar la lógica de negocios en tiempo de ejecución para calificar el acceso. Para obtener información sobre cómo calificar el acceso con la lógica de negocios, consulte [acceso de calificación con lógica de negocios en script](qualifying-access-with-business-logic-in-script.md).

En el ejemplo siguiente se muestra cómo comprobar el acceso de un cliente a una operación. En el ejemplo se da por supuesto que hay un almacén de directivas XML denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada///Expense y una operación denominada UseFormControl.


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



 

 



