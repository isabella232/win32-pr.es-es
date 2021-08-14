---
description: Especificar cifrados de Schannel y puntos fuertes de cifrado
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Especificar cifrados de Schannel y puntos fuertes de cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ef036038c3c0f759bdf4f2c2d18f0ac005ac01563d2779c5fcac02999fe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917281"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Especificar cifrados de Schannel y puntos fuertes de cifrado

Para los intercambios de información de cliente/servidor, el comportamiento predeterminado de Schannel es negociar el mejor cifrado disponible en función de los habilitados en el Registro. Las aplicaciones pueden limitar los cifrados y los puntos de cifrado permitidos para una conexión mediante el uso de miembros de la estructura [**\_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) de SCHANNEL como se muestra a continuación:

1.  Establezca el **miembro palgSupportedAlgs en** una matriz de [**id. de ALG \_**](../seccrypto/alg-id.md) que contenga los cifrados permitidos. Para obtener más información, vea Cipher IDs (IDs de cifrado).
2.  Establezca los **miembros dwMinimumCipherStrength** o **dwMaximumCipherStrength** en los niveles mínimo y máximo permitidos. Para obtener más información, vea Valores de intensidad de cifrado.
3.  Pase la [**estructura \_ CRED de SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por medio del *parámetro pAuthData)* en una llamada a la [**función AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Esta función devuelve un identificador de credenciales.
4.  Especifique el identificador de credenciales en una llamada a la función [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) del lado cliente o a la función [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) del lado servidor.

## <a name="cipher-ids"></a>IDs de cifrado

El comportamiento predeterminado de Schannel es solicitar el mejor cifrado disponible en función de las entradas de Schannel en el registro del sistema. No cambie el registro del sistema; la configuración que contiene para Schannel se usa globalmente y afectará a otras aplicaciones. Para obtener la lista de constantes válidas, vea [**ALG \_ ID**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Valores de intensidad de cifrado

Esta característica de Schannel se usa normalmente para limitar una conexión a cifrados nacionales o de intensidad de exportación. Los puntos fuertes nacionales incluyen 56 y 128 bits, mientras que la intensidad de exportación se limita a 56 bits. Si establece los valores mínimo y máximo en cero, Schannel usará todos los niveles de cifrado disponibles.

Con TLS o SSL 3.0, establezca el miembro **dwMinimumCipherStrength** en -1 (negativo) para habilitar los conjuntos de cifrado "Cifrado nulo", que proporcionan firmas pero no cifrado. Si **dwMaximumCipherStrength** también se establece en -1, solo se habilitarán los conjuntos de "cifrado nulo". Esta configuración está pensada solo para desarrollo y no debe usarse en sistemas de producción.

## <a name="querying-cipher-information"></a>Consulta de información de cifrado

Para recuperar la configuración de nivel de cifrado de una credencial, llame a la función [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) y especifique SECPKG \_ ATTR CIPHER STRENGTHS como parámetro \_ \_ *ulAttribute.*

Para recuperar la lista de algoritmos admitidos para una credencial, llame a [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) con SECPKG \_ ATTR SUPPORTED ALGS como parámetro \_ \_ *ulAttribute.*

 

 
