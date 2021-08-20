---
title: Publicación con el servicio de nombres RPC
description: Los servicios RPC pueden publicar sus identificadores en un espacio de nombres mediante las API del servicio de nombres RPC (RPCN).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publicación con RPC Name Service AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd53922bd4ce952c18c58d1b71cb485887bdc0fd020f4113679eb114b32b6f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025373"
---
# <a name="publishing-with-the-rpc-name-service"></a>Publicación con el servicio de nombres RPC

Los servicios RPC pueden publicar sus identificadores en un espacio de nombres mediante las API del servicio de nombres RPC (RPCN). Las API rpcNs de Windows 2000 publican las entradas RPC en Active Directory Domain Services. Los servicios crean enlaces RPC y los publican en el espacio de nombres como entradas de servidor RPC con nombre con atributos, incluido el identificador de interfaz único, un GUID reconocido por los clientes. A continuación, un cliente puede buscar servidores RPC que ofrecen la interfaz deseada, importar el enlace y conectarse al servidor.

Para obtener más información sobre cómo publicar un servicio RPC, vea [Enlace del lado servidor.](/windows/desktop/Rpc/server-side-binding)

 

 