---
description: El campo de la criptografía es grande y en aumento.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipos de proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e976909cec25b5194187d61d2e753eeb830c09f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809337"
---
# <a name="cryptographic-provider-types"></a>Tipos de proveedor de servicios criptográficos

El campo de la [*Criptografía*](../secgloss/c-gly.md) es grande y en aumento. Existen muchos protocolos y formatos de datos estándar diferentes. Generalmente, se organizan en grupos o familias, cada uno de los cuales tiene su propio conjunto de formatos de datos y forma de realizar cosas. Incluso si dos familias usan el mismo algoritmo (por ejemplo, el [](../secgloss/r-gly.md) [*cifrado de bloques*](../secgloss/b-gly.md)de RC2), a menudo usarán diferentes esquemas de [*relleno*](../secgloss/p-gly.md) , diferentes [*longitudes de clave*](../secgloss/k-gly.md)y diferentes modos predeterminados. CryptoAPI está diseñado de modo que un tipo de proveedor de CSP representa una familia determinada.

Cuando una aplicación se conecta a un CSP de un tipo determinado, cada una de las funciones de CryptoAPI funcionará de forma predeterminada de acuerdo con la familia que corresponde a ese tipo de CSP. La elección del tipo de proveedor de una aplicación especifica los siguientes elementos:



| Elemento                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo de intercambio de claves*](../secgloss/k-gly.md)                | Cada tipo de proveedor especifica uno y solo un algoritmo de intercambio de claves. Cada CSP de un tipo determinado debe implementar este algoritmo. Las aplicaciones especifican el algoritmo de intercambio de claves que se va a utilizar seleccionando un CSP del tipo de proveedor adecuado.                                                        |
| [*Algoritmo de firma digital*](../secgloss/d-gly.md) | Cada tipo de proveedor especifica uno y solo un algoritmo de firma digital. Cada CSP de un tipo determinado debe implementar este algoritmo. Las aplicaciones especifican el algoritmo de firma digital que se va a utilizar seleccionando un CSP del tipo de proveedor adecuado.                                              |
| Formatos BLOB de clave                                                                                                                    | El tipo de proporcionar determina el formato del [*BLOB de clave*](../secgloss/k-gly.md) que se usa para exportar las claves del [*CSP*](../secgloss/c-gly.md) y para importar las claves en un CSP. |
| Formato de firma digital                                                                                                            | El tipo de proveedor determina el formato de la firma digital. Esto garantiza que cualquier CSP del mismo tipo de proveedor puede comprobar una firma generada por un CSP de un tipo de proveedor determinado.                                                                                                              |
| Esquema de derivación de claves de sesión                                                                                                       | El tipo de proveedor determina el método que se usa para derivar una [*clave de sesión*](../secgloss/s-gly.md) de un [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Longitud de la clave*](../secgloss/k-gly.md)                                                    | Algunos tipos de proveedor especifican la longitud de los [*pares de claves pública y privada*](../secgloss/p-gly.md) y las claves de sesión.                                                                                                               |
| Modos predeterminados                                                                                                                       | El tipo de proveedor a menudo especifica los modos predeterminados para varias opciones, como el [*modo*](../secgloss/c-gly.md) de cifrado de cifrado de bloqueo o el método de [*relleno*](../secgloss/p-gly.md) de cifrado de bloque.          |



 

Es posible que algunas aplicaciones avanzadas se conecten a más de un CSP a la vez, pero la mayoría de las aplicaciones suelen usar un solo CSP.

Actualmente hay una serie de tipos de proveedor predefinidos. En las secciones siguientes se proporciona información sobre los siguientes tipos de proveedor:

-   [aprovisionamiento \_ completo de RSA \_](prov-rsa-full.md)
-   [\_AES de RSA \_](prov-rsa-aes.md)
-   [\_firma RSA \_ SIG](prov-rsa-sig.md)
-   [aprovisionamiento de \_ RSA \_ Schannel](prov-rsa-schannel.md)
-   [DSS de PROV \_](prov-dss.md)
-   [de PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ Schannel](prov-dh-schannel.md)
-   [Fortezza de PROV \_](prov-fortezza.md)
-   [\_Microsoft \_ Exchange](prov-ms-exchange.md)
-   [SSL de PROV \_](prov-ssl.md)

Aunque algunos tipos de CSP pueden ser parcialmente compatibles con otros, dos o más aplicaciones que necesitan [*intercambiar claves*](../secgloss/e-gly.md) y mensajes cifrados deben usar CSP del mismo tipo.

Un escritor de CSP personalizado puede definir un nuevo tipo de proveedor. Sin embargo, el escritor de CSP es responsable de distribuir el nuevo tipo de proveedor a los autores de las aplicaciones que lo utilizan. Para obtener información sobre cómo escribir CSP personalizados, consulte [proveedores de servicios de cifrado](cryptographic-service-providers.md).

 

 
