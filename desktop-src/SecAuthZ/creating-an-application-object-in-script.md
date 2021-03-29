---
description: Para cada aplicación que usa un almacén de directivas de autorización, debe crear un objeto IAzApplication y, a continuación, guardarlo en un almacén de directivas.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Crear un objeto de aplicación en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811270"
---
# <a name="creating-an-application-object-in-script"></a>Crear un objeto de aplicación en el script

Un almacén de directivas de autorización contiene información de directiva de autorización para una o más aplicaciones. Para cada aplicación que usa un almacén de directivas de autorización, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.

En el ejemplo siguiente se muestra cómo crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representa una aplicación y cómo agregar el objeto **IAzApplication** al almacén de directivas de autorización que usa la aplicación. En el ejemplo se da por supuesto que hay un almacén de directivas XML con el nombre MyStore.xml en el directorio raíz de la unidad C.


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



 

 



