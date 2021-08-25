---
description: El campo de criptografía es grande y está creciendo.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipos de proveedor de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaeee585ff9c11e2a20a201f541f3cd147aef6e9b50c37d60156e75a1b9fd94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876215"
---
# <a name="cryptographic-provider-types"></a>Tipos de proveedor de servicios criptográficos

El campo de [*criptografía*](../secgloss/c-gly.md) es grande y está creciendo. Hay muchos protocolos y formatos de datos estándar diferentes. Por lo general, se organizan en grupos o familias, cada uno de los cuales tiene su propio conjunto de formatos de datos y forma de hacer las cosas. Incluso si dos familias usan el mismo algoritmo (por ejemplo, el [](../secgloss/p-gly.md) cifrado de [*bloques RC2),*](../secgloss/r-gly.md) [](../secgloss/b-gly.md)a menudo usarán esquemas de relleno diferentes, longitudes de clave diferentes y modos predeterminados diferentes. [](../secgloss/k-gly.md) CryptoAPI está diseñado para que un tipo de proveedor csp represente una familia determinada.

Cuando una aplicación se conecta a un CSP de un tipo determinado, cada una de las funciones cryptoAPI funcionará de forma predeterminada de una manera prescrita por la familia correspondiente a ese tipo de CSP. La elección del tipo de proveedor de una aplicación especifica los siguientes elementos:



| Elemento                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo de intercambio de claves*](../secgloss/k-gly.md)                | Cada tipo de proveedor especifica un único algoritmo de intercambio de claves. Cada CSP de un tipo determinado debe implementar este algoritmo. Las aplicaciones especifican el algoritmo de intercambio de claves que se usará seleccionando un CSP del tipo de proveedor adecuado.                                                        |
| [*Algoritmo de firma digital*](../secgloss/d-gly.md) | Cada tipo de proveedor especifica un único algoritmo de firma digital. Cada CSP de un tipo determinado debe implementar este algoritmo. Las aplicaciones especifican el algoritmo de firma digital que se usará seleccionando un CSP del tipo de proveedor adecuado.                                              |
| Formatos de BLOB de clave                                                                                                                    | El tipo provide determina el formato del [*blob*](../secgloss/k-gly.md) de clave que se usa para exportar claves del [*CSP*](../secgloss/c-gly.md) e importar claves en un CSP. |
| Formato de firma digital                                                                                                            | El tipo de proveedor determina el formato de firma digital. Esto garantiza que cualquier CSP del mismo tipo de proveedor pueda comprobar una firma producida por un CSP de un tipo de proveedor determinado.                                                                                                              |
| Esquema de derivación de claves de sesión                                                                                                       | El tipo de proveedor determina el método utilizado para derivar una clave de [*sesión*](../secgloss/s-gly.md) de un [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Longitud de clave*](../secgloss/k-gly.md)                                                    | Algunos tipos de proveedor especifican la longitud de [*los pares de claves pública*](../secgloss/p-gly.md) y privada y las claves de sesión.                                                                                                               |
| Modos predeterminados                                                                                                                       | El tipo de proveedor a menudo especifica los modos predeterminados para varias opciones, como el modo de cifrado de [*cifrado*](../secgloss/c-gly.md) de bloques o el método de relleno de [*cifrado de*](../secgloss/p-gly.md) bloques.          |



 

Es posible que alguna aplicación avanzada se conecte a más de un CSP a la vez, pero la mayoría de las aplicaciones suelen usar solo un único CSP.

Actualmente hay una serie de tipos de proveedor predefinidos. En las secciones siguientes se proporciona información sobre los siguientes tipos de proveedor:

-   [PROV \_ RSA \_ FULL](prov-rsa-full.md)
-   [PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROV \_ RSA \_ SCHANNEL](prov-rsa-schannel.md)
-   [PROV \_ DSS](prov-dss.md)
-   [PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ SCHANNEL](prov-dh-schannel.md)
-   [PROV \_ FORTEZZA](prov-fortezza.md)
-   [PROV \_ MS \_ EXCHANGE](prov-ms-exchange.md)
-   [PROV \_ SSL](prov-ssl.md)

Aunque algunos tipos de CSP pueden ser parcialmente compatibles con [](../secgloss/e-gly.md) otros, dos o más aplicaciones que necesitan intercambiar claves y mensajes cifrados deben usar CSP del mismo tipo.

Un escritor de CSP personalizado puede definir un nuevo tipo de proveedor. Sin embargo, el escritor de CSP es responsable de distribuir el nuevo tipo de proveedor a los autores de cualquier aplicación que lo use. Para obtener información sobre cómo escribir LOSPS personalizados, vea [Proveedores de servicios criptográficos](cryptographic-service-providers.md).

 

 
