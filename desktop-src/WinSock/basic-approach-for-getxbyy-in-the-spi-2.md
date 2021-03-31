---
description: La mayoría de las funciones de GetXbyY se traducen mediante Ws2 \_32.dll a una secuencia WSALookupServiceBegin, WSALookupServiceNext, WSALookupServiceEnd que usa uno de los conjuntos de GUID especiales como clase de servicio.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Enfoque básico para GetXbyY en SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907959"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a>Enfoque básico para GetXbyY en SPI

La mayoría de las funciones de **GetXbyY** se traducen mediante Ws2 \_32.dll a una secuencia [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALOOKUPSERVICEEND**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) que usa uno de los conjuntos de GUID especiales como clase de servicio. Estos GUID identifican el tipo de operación **GetXbyY** que se está emulando. La consulta está restringida a los NSP que admiten AF \_ inet. Siempre que una función **GetXbyY** devuelve una estructura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) o [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) , el \_32.dll Ws2 especificará la \_ marca LUP REturn \_ BLOB en **WSALookupServiceBegin** para que el NSP devuelva la información deseada. Estas estructuras deben modificarse ligeramente en que los punteros contenidos en deben reemplazarse por desplazamientos que son relativos al inicio de los datos del BLOB. Todos los valores a los que hacen referencia estos miembros de puntero deben, por supuesto, estar contenidos completamente dentro del BLOB y todas las cadenas son ASCII.

 

 



