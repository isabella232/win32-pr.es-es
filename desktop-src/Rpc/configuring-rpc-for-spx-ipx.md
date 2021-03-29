---
title: Configuración de RPC para SPX/IPX
description: Al usar los \_ transportes ncacn SPX y ncadg \_ IPX, el nombre del servidor es exactamente el mismo que el nombre del servidor en Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486915"
---
# <a name="configuring-rpc-for-spxipx"></a>Configuración de RPC para SPX/IPX

Al usar los transportes **ncacn \_ SPX** y **ncadg \_ IPX** , el nombre del servidor es exactamente el mismo que el nombre del servidor en Windows. Sin embargo, puesto que los nombres se distribuyen mediante protocolos de Novell, deben cumplir las convenciones de nomenclatura de Novell. Si un nombre de servidor no es un nombre de Novell válido, los servidores no podrán crear extremos con los transportes **ncacn \_ SPX** o **ncadg \_ IPX** .

Un nombre de servidor Novell válido solo contiene los caracteres entre 0x20 y 0x7F. Los caracteres en minúsculas se cambian a mayúsculas. No se pueden usar los siguientes caracteres:

" \* ,./:; <=>?\[\]\\\|\]

Para mantener la compatibilidad con la primera versión de Windows NT, **ncacn \_ SPX** y **ncadg \_ IPX** también permiten usar un formato especial del nombre del servidor conocido como el nombre de la tilde. El nombre de la tilde se compone de una tilde (~), seguida del número de red de ocho dígitos del servidor y, a continuación, seguido de su dirección Ethernet de 12 dígitos. Los nombres de tildes tienen una ventaja en que no requieren ninguna funcionalidad de servicio de nombres. Por lo tanto, si está conectado a un servidor, el nombre de la tilde funcionará.

Las tablas siguientes contienen dos configuraciones de ejemplo que ilustran los puntos descritos anteriormente.



| Componente                            | Configurado como      |
|--------------------------------------|--------------------|
| Windows Server                       | NWCS               |
| Cliente Windows                       | NWCS               |
| cliente de Windows de 16 bits, cliente de MS-DOS | Redirector de NetWare |



 

La configuración de la tabla anterior requiere que tenga servidores de archivos de NetWare o enrutadores en la red. Generará el mejor rendimiento porque los nombres de servidor se almacenan en el enlace de NetWare.



| Componente                            | Configurado como |
|--------------------------------------|---------------|
| Windows Server                       | Agente SAP     |
| Cliente Windows                       | IPX/SPX       |
| cliente de Windows de 16 bits, cliente de MS-DOS | IPX/SPX       |



 

La segunda configuración funciona en un entorno que no contiene servidores de archivos de NetWare o enrutadores (por ejemplo, una red de dos equipos: un servidor de Windows y un cliente de MS-DOS). La resolución de nombres, que se realiza durante la primera llamada a través de un identificador de enlace, será ligeramente más lenta que en la primera configuración. Además, la segunda configuración produce más tráfico generado a través de la red.

Para implementar la resolución de nombres, cuando un servidor RPC usa un extremo SPX o IPX, el nombre del servidor y el punto de conexión se registran como un servidor de protocolo de anuncio de servicio (SAP) de tipo 640 (hexadecimal). Para resolver un nombre de servidor, el cliente RPC envía una solicitud de SAP para todos los servicios del mismo tipo y, a continuación, examina la lista de respuestas para el nombre del servidor. Este proceso se produce durante la primera llamada RPC sobre cada identificador de enlace. Para obtener más información sobre el protocolo SAP para Novell, consulte la documentación de NetWare.

> [!Note]  
> Las aplicaciones cliente de Windows de 16 bits que usan los transportes **ncacn \_ SPX** o **ncadg \_ ipx** requieren que el archivo Nwipxspx.dll instalarse para ejecutarse en el subsistema wow. Póngase en contacto con Novell para obtener este archivo.

 

 

 




