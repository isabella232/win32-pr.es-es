---
description: Ws232.dll traduce la mayoría de las funciones GetXbyY a una secuencia \_ WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa uno de un conjunto de GUID especiales como la clase de servicio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Enfoque básico de GetXbyY en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba707747dd6082bfa6c8b3c4dd3c19e8d6ce968359745947227ee464d97f984f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560529"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Enfoque básico de GetXbyY en spi

La mayoría de las funciones **GetXbyY** se traducen mediante Ws232.dll a una secuencia \_ [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de un conjunto de GUID especiales como la clase de servicio. Estos GUID identifican el tipo de operación **GetXbyY** que se va a emular. La consulta está restringida a los NSP que admiten AF \_ INET. Cada vez que una función **GetXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERSERVICIO,**](/windows/desktop/api/winsock/ns-winsock-servent) el32.dll Ws2 especificará la marca LUP RETURN BLOB en \_ \_ \_ **WSALookupServiceBegin** para que el NSP devuelva la información deseada. Estas estructuras deben modificarse ligeramente, ya que los punteros contenidos en deben reemplazarse por desplazamientos relativos al inicio de los datos del blob. Por supuesto, todos los valores a los que hacen referencia estos miembros de puntero deben estar contenidos completamente en el blob y todas las cadenas son ASCII.

 

 



