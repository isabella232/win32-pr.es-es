---
description: CryptoAPI se ha diseñado para que sea fácilmente extensible. Cualquier autor de proveedor de servicios criptográficos (CSP) puede definir nuevos tipos y parámetros para que CryptoAPI se adete a los requisitos de una amplia variedad de situaciones.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Extensión de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0538e15f49e61dc26cacd4e81c42dd462aec092877428ebe865ab97c7729f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007031"
---
# <a name="extending-cryptoapi"></a>Extensión de CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) se ha diseñado para que sea fácilmente extensible. Cualquier autor de proveedor de [](../secgloss/c-gly.md) servicios criptográficos (CSP) puede definir nuevos tipos y parámetros para que CryptoAPI se adete a los requisitos de una amplia variedad de situaciones.



| Elementos extensibles                                                                                                 | Comentario                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipos de proveedor<br/>                                                                                        | Un tipo de proveedor representa una familia o un tipo determinados de servicios criptográficos. Se pueden definir nuevos tipos de proveedor, cada uno de los que sirve a un sector determinado.<br/>                                                                                                                                                                                                                                                                                          |
| Parámetros del proveedor<br/>                                                                                   | Los parámetros del proveedor se envían y reciben [**mediante CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) y [**CPGetProvParam,**](https://www.bing.com/search?q=**CPGetProvParam**)respectivamente. Los nuevos parámetros de proveedor podrían permitir que un CSP se configurara de maneras no previstas por los diseñadores cryptoAPI.<br/>                                                                                                                                                                 |
| Identificadores de algoritmo<br/>                                                                                 | Las instalaciones de enumeración [**de CPGetProvParam permiten**](https://www.bing.com/search?q=**CPGetProvParam**) a las aplicaciones enumerar identificadores de algoritmo dinámicamente. Los [*nuevos algoritmos*](../secgloss/s-gly.md) [*simétricos, de*](../secgloss/p-gly.md)clave pública y [*hash*](../secgloss/h-gly.md) se pueden definir en cualquier momento.<br/> |
| Tipos de par [*de claves pública y*](../secgloss/p-gly.md) privada<br/> | Aunque los nuevos tipos de par de claves se pueden definir según sea necesario, actualmente solo se usan pares de claves de firma [*e*](../secgloss/e-gly.md) intercambio de claves.<br/>                                                                                                                                                                                                                                           |
| Tipos de BLOB de clave<br/>                                                                                        | Los nuevos tipos [*de blobs*](../secgloss/b-gly.md) en claves podrían permitir el intercambio de claves de sesión, claves públicas y pares de claves públicas y privadas de una manera flexible mediante las funciones [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) y [**CPImportKey.**](https://www.bing.com/search?q=**CPImportKey**)<br/>                                                                                                                                            |
| Parámetros clave<br/>                                                                                        | Los parámetros clave se envían y recuperan [**mediante CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) [**y CPGetKeyParam.**](https://www.bing.com/search?q=**CPGetKeyParam**) Los nuevos parámetros de clave podrían habilitar la compatibilidad con muchos tipos diferentes de claves.<br/>                                                                                                                                                                                                                         |
| Parámetros de objeto hash<br/>                                                                                | Los parámetros de objeto hash se envían y recuperan [**mediante CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) [**y CPGetHashParam.**](https://www.bing.com/search?q=**CPGetHashParam**) Los nuevos parámetros de objeto hash podrían habilitar la compatibilidad con muchos tipos diferentes [*de hashes*](../secgloss/h-gly.md).<br/>                                                                                                                                         |
| Valores de marca<br/>                                                                                           | La mayoría de las funciones CryptoAPI/CryptoSPI tienen *un parámetro dwFlags.* Los *nuevos valores dwFlags* podrían modificar el comportamiento de las funciones según sea necesario.<br/>                                                                                                                                                                                                                                                                                                       |



 

Las extensiones de CryptoAPI deben realizarse de forma responsable. Antes de definir nuevos parámetros y tipos de algoritmo, un desarrollador de CSP debe consultar Microsoft Corporation, de modo que:

-   Las extensiones comunes de CryptoAPI se pueden identificar y colocar en el archivo Wincrypt.h estándar.
-   Se pueden evitar conflictos de espacios de nombres.
-   Se puede determinar si la extensión es necesaria o si se puede lograr una operación determinada mediante la API actual.

> [!Note]  
> Para que un CSP sea compatible con las aplicaciones desarrolladas para el proveedor de servicios criptográficos base de Microsoft, debe admitir todos los elementos anteriores, como se describe en [Funciones](cryptography-functions.md) de criptografía base y en Funciones del proveedor de servicios [criptográficos](cryptography-functions.md).

 

 

 
