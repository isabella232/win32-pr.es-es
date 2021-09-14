---
description: La información de este tema se aplica a Windows Server 2003 y Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Capa de sockets seguros protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265500"
---
# <a name="secure-sockets-layer-protocol"></a>Capa de sockets seguros protocolo

La información de este tema se aplica a Windows Server 2003 y Windows XP. Para obtener conjuntos de cifrado para Windows Server 2008 y Windows Vista, vea Conjuntos de [cifrado en Schannel](cipher-suites-in-schannel.md).

Schannel admite las versiones 2.0 y 3.0 del [*protocolo Capa de sockets seguros (SSL).*](../secgloss/s-gly.md)

> [!Note]  
> A partir Windows 10 versión 1607 y Windows Server 2016, SSL 2.0 se ha quitado y ya no se admite.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3.0 es el predecesor del Protocolo de seguridad de la [capa de transporte.](transport-layer-security-protocol.md)

Schannel admite los conjuntos de cifrado enumerados en [Conjuntos de cifrado TLS](tls-cipher-suites.md) para SSL 3.0. SSL 3.0 admite todos los conjuntos de cifrado enumerados en Conjuntos de cifrado TLS, así como SSL \_ FORTEZZA \_ KEA \_ WITH \_ FORTEZZA \_ CBC \_ SHA.

## <a name="ssl-20"></a>SSL 2.0

SSL 2.0 se ha reemplazado por TLS y no debe usarse para el nuevo desarrollo.

Schannel admite los siguientes conjuntos de cifrado para SSL 2.0. Los conjuntos se enumeran en orden de más seguro a menos seguro.

-   SSL \_ RC4 \_ 128 \_ WITH \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ CON \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ WITH \_ MD5
-   SSL \_ DES \_ 64 \_ CBC \_ WITH \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5

 

 
