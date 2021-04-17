---
description: Especificar cifrados Schannel y niveles de cifrado
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Especificar cifrados Schannel y niveles de cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668254"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Especificar cifrados Schannel y niveles de cifrado

Para los intercambios de información de cliente/servidor, el comportamiento predeterminado de Schannel es negociar el mejor cifrado disponible en función de los habilitados en el registro. Las aplicaciones pueden limitar los cifrados y los niveles de cifrado permitidos para una conexión mediante el uso de miembros de la estructura de [**\_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) de la siguiente manera:

1.  Establezca el miembro **palgSupportedAlgs** en una matriz de [**\_ ID**](../seccrypto/alg-id.md) . de alg que contenga los cifrados permitidos. Para obtener más información, vea identificadores de cifrado.
2.  Establezca los miembros **dwMinimumCipherStrength** y/o **dwMaximumCipherStrength** en los valores mínimo y máximo permitidos. Para obtener más información, vea valores de intensidad de cifrado.
3.  Pase la [**estructura \_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por medio del parámetro *pAuthData* ) en una llamada a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Esta función devuelve un identificador de credenciales.
4.  Especifique el identificador de credenciales en una llamada a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) del lado cliente o la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) del lado servidor.

## <a name="cipher-ids"></a>Identificadores de cifrado

El comportamiento predeterminado de Schannel es solicitar el mejor cifrado disponible en función de las entradas Schannel en el registro del sistema. No cambie el registro del sistema; la configuración que contiene Schannel se usa globalmente y afectará a otras aplicaciones. Para obtener la lista de constantes válidas, [**consulte \_ ID**](../seccrypto/alg-id.md). de ALG.

## <a name="cipher-strength-values"></a>Valores de intensidad de cifrado

Esta característica de Schannel se usa normalmente para limitar una conexión a los cifrados de fuerza de exportación o nacionales. Entre las fortalezas internas se incluyen 56 y 128 bits, mientras que el nivel de exportación está limitado a 56 bits. Si establece los valores mínimo y máximo en cero Schannel, se usarán todos los niveles de cifrado disponibles.

Con TLS o SSL 3,0, establezca el miembro **dwMinimumCipherStrength** en-1 (menos uno) para habilitar los conjuntos de cifrado "cifrado null", que proporcionan firmas pero no cifrado. Si **dwMaximumCipherStrength** también se establece en-1, solo se habilitarán los conjuntos de "cifrado null". Esta configuración está pensada solo para el desarrollo y no debe usarse en sistemas de producción.

## <a name="querying-cipher-information"></a>Consultar información de cifrado

Para recuperar la configuración de la intensidad de cifrado de una credencial, llame a la función [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) y especifique SECPKG \_ ATTR \_ Cipher Strength \_ como el parámetro *ulAttribute* .

Para recuperar la lista de algoritmos admitidos para una credencial, llame a [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) con SECPKG \_ ATTR \_ compatible \_ ALGS como parámetro *ulAttribute* .

 

 
