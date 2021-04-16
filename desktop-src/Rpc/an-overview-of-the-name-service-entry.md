---
title: Información general de la entrada del servicio de nombres
description: La entrada servicio de nombres consta de tres secciones distintas.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676267"
---
# <a name="an-overview-of-the-name-service-entry"></a>Información general de la entrada del servicio de nombres

La entrada servicio de nombres consta de tres secciones distintas. La primera sección es para las interfaces (UUID + versión), la segunda contiene el objeto UUID y la tercera sección es para los identificadores de enlace. Proporcione un nombre para la entrada que sirva como una manera de identificarla.

Al llamar a [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), el servidor especifica el nombre de la entrada en la que se va a colocar la información exportada. Esta nueva interfaz exportada se agrega a continuación a la sección interfaz de la entrada servicio de nombres. También se conservan las interfaces que ya están presentes en la entrada del servicio de nombres. Este mismo proceso se sigue para los UUID de objeto y los identificadores de enlace.

El cliente llama a [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) para buscar un identificador de enlace adecuado. Se extraen el nombre de la entrada, el identificador de interfaz y el UUID de un objeto. Estos restringen las entradas de las que se devuelven los identificadores de enlace. Si una entrada coincide con los criterios de búsqueda, todos los identificadores de enlace de esa entrada se devuelven desde [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).

 

 




