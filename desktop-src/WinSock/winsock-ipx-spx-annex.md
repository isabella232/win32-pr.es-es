---
description: En esta sección se describen las extensiones de Winsock específicas de paquetes de trabajo Exchange/secuenciado de paquetes Exchange (IPX/SPX). También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o pueden presentar un comportamiento único.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Anexo de WINSOCK IPX/SPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051353"
---
# <a name="winsock-ipxspx-annex"></a>Anexo de WINSOCK IPX/SPX

En esta sección se describen las extensiones de Winsock específicas de paquetes de trabajo Exchange/secuenciado de paquetes Exchange (IPX/SPX). También se describen aspectos de las funciones base de Winsock que requieren una consideración especial o pueden presentar un comportamiento único.



| Elemento          | Descripción                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombres de protocolo | IPX, SPX                                                                                                                                        |
| Descripción      | Proporciona servicios de transporte a través de la capa de red IPX: IPX para datagramas no confiables, SPX para flujos de mensajes confiables orientados a la conexión. |
| Familia de direcciones   | AF \_ IPX                                                                                                                                         |
| Archivo de encabezado      | Wsipx.h                                                                                                                                         |



 

En esta sección se describe cómo usar Winsock con la familia de protocolos IPX, lo que permite que las aplicaciones IPX tradicionales se porte a Winsock. Las redes IPX funcionan de una manera fundamentalmente diferente a las redes IP, por lo que estas diferencias deben tenerse en cuenta al usar IPX/SPX.

 

 



