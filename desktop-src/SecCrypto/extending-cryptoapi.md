---
description: CryptoAPI se ha diseñado para ser fácilmente extensible. Cualquier autor de proveedor de servicios criptográficos (CSP) puede definir nuevos tipos y parámetros para hacer que CryptoAPI se pliegue a los requisitos de una amplia variedad de situaciones.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Extensión de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62417f66b8a8bb2d06d145543f944f91868d366d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669731"
---
# <a name="extending-cryptoapi"></a>Extensión de CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) se ha diseñado para ser fácilmente extensible. Cualquier autor de [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) puede definir nuevos tipos y parámetros para hacer que CryptoAPI se pliegue a los requisitos de una amplia variedad de situaciones.



| Elementos extensibles                                                                                                 | Comentario                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipos de proveedor<br/>                                                                                        | Un tipo de proveedor representa una familia determinada o un tipo de servicios criptográficos. Se pueden definir nuevos tipos de proveedor, y cada uno de ellos sirve a un nicho determinado.<br/>                                                                                                                                                                                                                                                                                          |
| Parámetros de proveedor<br/>                                                                                   | Los parámetros de proveedor se envían y se reciben mediante [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) y [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**), respectivamente. Los nuevos parámetros de proveedor podrían permitir la configuración de un CSP de maneras no previstas por los diseñadores de CryptoAPI.<br/>                                                                                                                                                                 |
| Identificadores de algoritmo<br/>                                                                                 | Las funciones de enumeración de [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**) permiten a las aplicaciones enumerar los identificadores de algoritmo dinámicamente. En cualquier momento se pueden definir nuevos algoritmos [*simétricos*](../secgloss/s-gly.md), [*clave pública*](../secgloss/p-gly.md)y [*hash*](../secgloss/h-gly.md) .<br/> |
| Tipos de pares de claves pública y [*privada*](../secgloss/p-gly.md)<br/> | Aunque se pueden definir nuevos tipos de pares de claves según sea necesario, actualmente solo se usan [*pares de claves de intercambio*](../secgloss/e-gly.md) de claves y firma.<br/>                                                                                                                                                                                                                                           |
| Tipos de BLOB de clave<br/>                                                                                        | Los nuevos tipos de [*BLOB*](../secgloss/b-gly.md) de clave pueden permitir que las claves de sesión, las claves públicas y los pares de claves pública y privada se intercambien de forma flexible con las funciones [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) y [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) .<br/>                                                                                                                                            |
| Parámetros clave<br/>                                                                                        | Los parámetros de clave se envían y recuperan con [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) y [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**). Los nuevos parámetros de clave podrían habilitar la compatibilidad con muchos tipos diferentes de claves.<br/>                                                                                                                                                                                                                         |
| Parámetros de objeto hash<br/>                                                                                | Los parámetros de objeto hash se envían y recuperan con [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) y [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**). Los nuevos parámetros de objeto hash podrían habilitar la compatibilidad con muchos tipos diferentes de [*hashes*](../secgloss/h-gly.md).<br/>                                                                                                                                         |
| Valores de marca<br/>                                                                                           | La mayoría de las funciones CryptoAPI/CryptoSPI tienen un parámetro *dwFlags* . Los nuevos valores de *dwFlags* pueden modificar el comportamiento de las funciones según sea necesario.<br/>                                                                                                                                                                                                                                                                                                       |



 

Las extensiones de CryptoAPI deben realizarse de manera responsable. Antes de definir nuevos parámetros y tipos de algoritmo, un desarrollador de CSP debe consultar a Microsoft Corporation, de modo que:

-   Las extensiones CryptoAPI comunes se pueden identificar y colocar en el archivo de la estándar Wincrypt. h.
-   Se pueden evitar conflictos de espacio de nombres.
-   Se puede determinar si la extensión es necesaria o si se puede lograr una operación determinada mediante la API actual.

> [!Note]  
> Para que un CSP sea compatible con las aplicaciones desarrolladas para el proveedor de servicios criptográficos de base de Microsoft, debe admitir todos los elementos anteriores tal y como se describe en [funciones de criptografía base](cryptography-functions.md) y en [funciones de proveedor de servicios de criptografía](cryptography-functions.md).

 

 

 
