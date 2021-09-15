---
title: Información general de la entrada del servicio Name
description: La entrada del servicio de nombres consta de tres secciones distintas.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271839"
---
# <a name="an-overview-of-the-name-service-entry"></a>Información general de la entrada del servicio Name

La entrada del servicio de nombres consta de tres secciones distintas. La primera sección es para interfaces (UUID + versión), la segunda sección contiene los UUID del objeto y la tercera sección es para los identificadores de enlace. Proporcione un nombre para la entrada que sirva como forma de identificarla.

Al llamar [**a RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), el servidor especifica el nombre de la entrada en la que se va a colocar la información exportada. A continuación, esta interfaz recién exportada se agrega a la sección de interfaz de la entrada de servicio de nombre. Las interfaces que ya están presentes en la entrada del servicio de nombres también permanecen. Este mismo proceso se sigue para los UUID de objeto y los identificadores de enlace.

El cliente llama [**a RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin)**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)para buscar un identificador de enlace adecuado. Se extraen el nombre de entrada, el identificador de interfaz y un UUID de objeto. Restringen las entradas de las que se devuelven los identificadores de enlace. Si una entrada coincide con los criterios de búsqueda, todos los identificadores de enlace de esa entrada se devuelven de [**RpcNsBindingImportNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)

 

 




