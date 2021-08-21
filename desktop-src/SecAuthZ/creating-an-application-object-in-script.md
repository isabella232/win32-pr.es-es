---
description: Para cada aplicación que use un almacén de directivas de autorización, debe crear un objeto IAzApplication y, a continuación, guardarlo en un almacén de directivas.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Crear un objeto de aplicación en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 02a5ada4a8a79244cc454d9efc88e69a5d9a205241119b5dda371699f0c86552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782560"
---
# <a name="creating-an-application-object-in-script"></a>Crear un objeto de aplicación en script

Un almacén de directivas de autorización contiene información de directiva de autorización para una o varias aplicaciones. Para cada aplicación que use un almacén de directivas de autorización, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.

En el ejemplo siguiente se muestra cómo crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representa una aplicación y cómo agregar el objeto **IAzApplication** al almacén de directivas de autorización que usa la aplicación. En el ejemplo se supone que hay un almacén de directivas XML existente denominado MyStore.xml en el directorio raíz de la unidad C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



