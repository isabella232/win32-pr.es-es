---
description: En esta sección se describen las extensiones de Winsock específicas del intercambio de paquetes de interconexión/intercambio de paquetes secuenciados (IPX/SPX). También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden exhibir un comportamiento único.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de Winsock IPX/SPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705885"
---
# <a name="winsock-ipxspx-annex"></a>Anexo de Winsock IPX/SPX

En esta sección se describen las extensiones de Winsock específicas del intercambio de paquetes de interconexión/intercambio de paquetes secuenciados (IPX/SPX). También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden exhibir un comportamiento único.



| Elemento          | Descripción                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre (s) de protocolo | IPX, SPX                                                                                                                                        |
| Descripción      | Proporciona servicios de transporte a través de la capa de red IPX: IPX para datagramas no confiables, SPX para flujos de mensajes confiables y orientados a la conexión. |
| Familia de direcciones   | AF \_ IPX                                                                                                                                         |
| Archivo de encabezado      | WSIPX. h                                                                                                                                         |



 

En esta sección se describe cómo usar WinSock con la familia de protocolos de IPX, lo que permite migrar las aplicaciones de IPX tradicionales a Winsock. Las redes IPX funcionan de manera fundamentalmente diferente que las redes IP, por lo que se deben tener en cuenta tales diferencias al usar IPX/SPX.

 

 



