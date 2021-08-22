---
description: La consulta WSALookupServiceBegin usa SVCID \_ HOSTNAME como GUID de clase de servicio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Gethostname (Función) en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b610016222ab8a06ed874377be9ae447ad1d194ab9605a6e07b3cf829f520093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132268"
---
# <a name="gethostname-function-in-the-spi"></a>Gethostname (Función) en spi

La [**consulta WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ HOSTNAME como GUID de clase de servicio. Si *lpszServiceInstanceName* es null o hace referencia a una cadena null (es decir, . ""), el host local se va a resolver. De lo contrario, se producirá una búsqueda en un nombre de host especificado. Para emular [**gethostname,**](/windows/desktop/api/winsock/nf-winsock-gethostname) Ws232.dll especificará un puntero nulo para \_ *lpszServiceInstanceName* y especificará LUP RETURN NAME para que el nombre de host se devuelva en el parámetro \_ \_ *lpszServiceInstanceName.* Si una aplicación usa esta consulta y especifica LUP RETURN ADDR, la dirección host se proporciona en una estructura \_ \_ INFO de **CSADDR. \_** La acción LUP \_ RETURN BLOB no está definida para esta \_ consulta. El valor predeterminado de la información del puerto será cero a menos que *lpszQueryString* haga referencia a un servicio como ftp, en cuyo caso se suministrará la dirección de transporte completa del servicio indicado.

 

 



