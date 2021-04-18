---
description: La consulta WSALookupServiceBegin usa \_ el nombre de host SVCID como el GUID de la clase de servicio.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Función GetHostName (en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715128"
---
# <a name="gethostname-function-in-the-spi"></a>Función GetHostName (en el SPI

La consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa \_ el nombre de host SVCID como el GUID de la clase de servicio. Si *lpszServiceInstanceName* es null o hace referencia a una cadena nula (es decir, ""), el host local se va a resolver. De lo contrario, se producirá una búsqueda en un nombre de host especificado. Con el fin de emular [**GetHostName (**](/windows/desktop/api/winsock/nf-winsock-gethostname) , el \_ valor de Ws232.dll especificará un puntero nulo para *lpszServiceInstanceName* y especificará el nombre de retorno de LUP para \_ \_ que el nombre de host se devuelva en el parámetro *lpszServiceInstanceName* . Si una aplicación usa esta consulta y especifica LUP \_ Return \_ addr, la dirección del host se proporcionará en una estructura de **\_ información de CSADDR** . La \_ acción devolver \_ BLOB de LUP no está definida para esta consulta. La información del puerto se establecerá de forma predeterminada en cero, a menos que el *lpszQueryString* haga referencia a un servicio como FTP, en cuyo caso se proporcionará la dirección de transporte completa del servicio indicado.

 

 



