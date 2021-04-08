---
description: La información de este tema se aplica a Windows Server 2003 y Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocolo Capa de sockets seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001848"
---
# <a name="secure-sockets-layer-protocol"></a>Protocolo Capa de sockets seguros

La información de este tema se aplica a Windows Server 2003 y Windows XP. Para los conjuntos de cifrado para Windows Server 2008 y Windows Vista, consulte [conjuntos de cifrado en Schannel](cipher-suites-in-schannel.md).

Schannel admite las versiones 2,0 y 3,0 del [*protocolo capa de sockets seguros (SSL)*](../secgloss/s-gly.md).

> [!Note]  
> A partir de Windows 10, versión 1607 y Windows Server 2016, se ha quitado SSL 2,0 y ya no se admite.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3,0 es el predecesor del Protocolo de seguridad de la [capa de transporte](transport-layer-security-protocol.md).

Schannel admite los conjuntos de cifrado que aparecen en [conjuntos de cifrado TLS](tls-cipher-suites.md) para SSL 3,0. SSL 3,0 es compatible con todos los conjuntos de cifrado que se enumeran en conjuntos de cifrado TLS y SSL \_ Fortezza \_ Kea \_ con \_ Fortezza \_ CBC \_ Sha.

## <a name="ssl-20"></a>SSL 2.0

SSL 2,0 se ha sustituido por TLS y no debe usarse para el nuevo desarrollo.

Schannel admite los siguientes conjuntos de cifrado para SSL 2,0. Los conjuntos se muestran en orden de más seguro a menos seguro.

-   SSL \_ RC4 \_ 128 \_ con \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5
-   SSL \_ RC2 \_ CBC \_ \_ de 128 CBC \_ con \_ MD5
-   SSL \_ DES \_ 64 \_ CBC \_ con \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5

 

 
