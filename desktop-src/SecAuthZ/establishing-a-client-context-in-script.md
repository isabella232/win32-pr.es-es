---
description: Para establecer un contexto de cliente en script, una aplicación puede crear un contexto de cliente con un identificador para un token, un nombre de dominio y de usuario, o una representación de cadena del identificador de seguridad del cliente.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Establecer un contexto de cliente en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05a8ea51efa427c83e78c35806175712b3c6d0d66e0987909f98e23a081415e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913741"
---
# <a name="establishing-a-client-context-in-script"></a>Establecer un contexto de cliente en script

En el Administrador de autorización, una aplicación determina si un cliente tiene acceso a una operación llamando al método [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) de un objeto [**IAzClientContext,**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) que representa un contexto de cliente.

Una aplicación puede crear un contexto de cliente con un identificador para un [](/windows/desktop/SecGloss/s-gly) token, un dominio y un nombre de usuario, o una representación de cadena del identificador de seguridad (SID) del cliente.

Use los [**métodos InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)y [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) de un [**objeto IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) para crear un contexto de cliente.

En el ejemplo siguiente se muestra cómo crear un [**objeto IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) a partir de un nombre de cliente. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C y que este almacén contiene una aplicación denominada Expense.


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

%>
```



 

 
