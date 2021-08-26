---
title: Configuración de RPC para SPX/IPX
description: Al usar los transportes ncacn spx y \_ ncadg ipx, el nombre del servidor es exactamente el mismo que el nombre del \_ servidor en Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5557541b296c436f2c3c1de007eb0e331e1c77d0529be83e758a25b76ac5e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022455"
---
# <a name="configuring-rpc-for-spxipx"></a>Configuración de RPC para SPX/IPX

Al usar **los transportes ncacn \_ spx** y **ncadg \_ ipx,** el nombre del servidor es exactamente el mismo que el nombre del servidor en Windows. Sin embargo, dado que los nombres se distribuyen mediante protocolos de Nociones, deben ajustarse a las convenciones de nomenclatura de Nociones. Si un nombre de servidor no es un nombre válido de Noé, los servidores no podrán crear puntos de conexión con los transportes **ncacn \_ spx** o **ncadg \_ ipx.**

Un nombre de servidor de Nociones válido contiene solo los caracteres entre 0x20 y 0x7f. Los caracteres en minúsculas se cambian a mayúsculas. No se pueden usar los caracteres siguientes:

" \* ,./:;<=>?\[\]\\\|\]

Para mantener la compatibilidad con la primera versión de Windows NT, **ncacn \_ spx** y **ncadg \_ ipx** también permiten usar un formato especial del nombre del servidor conocido como nombre de tilde. El nombre de tilde consta de una tilde (~), seguida del número de red de ocho dígitos del servidor y, después, de su dirección Ethernet de 12 dígitos. Los nombres de tilde tienen una ventaja en que no requieren ninguna funcionalidad de servicio de nombres. Por lo tanto, si está conectado a un servidor, el nombre de tilde funcionará.

Las tablas siguientes contienen dos configuraciones de ejemplo que muestran los puntos descritos anteriormente.



| Componente                            | Configurado como      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Cliente Windows                       | NWCS               |
| Cliente de Windows de 16 bits, cliente MS-DOS | NetWare Redirector |



 

La configuración de la tabla anterior requiere que tenga enrutadores o servidores de archivos de NetWare en la red. Producirá el mejor rendimiento porque los nombres de servidor se almacenan en NetWare Bindery.



| Componente                            | Configurado como |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Cliente Windows                       | IPX/SPX       |
| Cliente de Windows de 16 bits, cliente MS-DOS | IPX/SPX       |



 

La segunda configuración funciona en un entorno que no contiene enrutadores o servidores de archivos de NetWare (por ejemplo, una red de dos equipos: un servidor Windows y un cliente MS-DOS). La resolución de nombres, que se realiza durante la primera llamada a través de un identificador de enlace, será ligeramente más lenta que en la primera configuración. Además, la segunda configuración genera más tráfico generado a través de la red.

Para implementar la resolución de nombres, cuando un servidor RPC usa un punto de conexión SPX o IPX, el nombre del servidor y el punto de conexión se registran como un servidor de Service Advertising Protocol (SAP) de tipo 640 (hexadecimal). Para resolver un nombre de servidor, el cliente RPC envía una solicitud de SAP para todos los servicios del mismo tipo y, a continuación, examina la lista de respuestas para el nombre del servidor. Este proceso se produce durante la primera llamada RPC a través de cada identificador de enlace. Para obtener información adicional sobre el protocolo SAP paraAje, consulte la documentación de NetWare.

> [!Note]  
> Las aplicaciones cliente de Windows de 16 bits que usan los transportes **ncacn \_ spx** o **ncadg \_ ipx** requieren que el archivo Nwipxspx.dll se instale para ejecutarse en el subsistema WOW. Póngase en contacto con Llegar a Para obtener este archivo.

 

 

 




