---
description: Llame al método IAzClientContext::AccessCheck para comprobar si el cliente tiene acceso a una o varias operaciones.
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Comprobación del acceso de cliente a los recursos solicitados en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7393001c63f0a5b605870a8498e76231f0bf620a8c7e819a8c624eace565499a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906705"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Comprobación del acceso de cliente a los recursos solicitados en el script

Llame al [**método AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un [**objeto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) para comprobar si el cliente tiene acceso a una o varias operaciones. Para obtener información sobre cómo crear **un objeto IAzClientContext,** vea [Establecer un contexto de cliente en script](establishing-a-client-context-in-script.md).

Un cliente podría pertenecer a más de un rol y una operación podría asignarse a más de una tarea, por lo que el Administrador de autorización comprueba todos los roles y tareas. Si algún rol al que pertenece el cliente contiene alguna tarea que contenga una operación, se concede acceso a esa operación.

Para comprobar el acceso de un solo rol al que pertenece el cliente, establezca la [**propiedad RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) del [**objeto IAzClientContext.**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext)

Al inicializar el almacén de directivas de autorización para la comprobación de acceso, debe pasar cero como valor del parámetro *lFlags* del método [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) del [**objeto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore)

También es posible aplicar lógica de negocios en tiempo de ejecución para calificar el acceso. Para obtener información sobre cómo calificar el acceso con lógica de negocios, vea [Acceso calificado con lógica de negocios en script](qualifying-access-with-business-logic-in-script.md).

En el ejemplo siguiente se muestra cómo comprobar el acceso de un cliente a una operación. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada Expense y una operación denominada UseFormControl.


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



 

 



