---
description: Las funciones de mensajes de CryptoAPI se adhieren al \# estándar de sintaxis de mensajes criptográficos (CMS) PKCS 7. Los desarrolladores deben estar familiarizados con esta especificación para usar de forma más eficaz las funciones de mensaje de bajo nivel. Aquí se resaltan algunas de sus definiciones.
ms.assetid: 99b633fe-9898-4570-ba8b-16ee78d351da
title: '\#Conceptos de sintaxis de mensajería CRIPTOGRÁFICA PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ead1c5e75737db80adbca725a30cb730b547be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668022"
---
# <a name="pkcs-7-cryptographic-messaging-syntax-concepts"></a>\#Conceptos de sintaxis de mensajería CRIPTOGRÁFICA PKCS 7

Las funciones de mensajes de CryptoAPI se adhieren al [estándar de sintaxis de mensajes criptográficos (CMS)](https://www.ietf.org/rfc/rfc3369.txt) [*PKCS \# 7*](../secgloss/p-gly.md) . Los desarrolladores deben estar familiarizados con esta especificación para usar de forma más eficaz las [*funciones de mensaje de bajo nivel*](../secgloss/l-gly.md). Aquí se resaltan algunas de sus definiciones.

El \# estándar PKCS 7 describe una sintaxis general para los datos a los que se puede aplicar la [*Criptografía*](../secgloss/c-gly.md) , como [*firmas digitales*](../secgloss/d-gly.md) y [*sobres digitales*](../secgloss/d-gly.md). La sintaxis tiene en cuenta la recursividad, de modo que, por ejemplo, un sobre puede estar anidado dentro de otro, o una parte puede firmar datos digitales que ya se han colocado en un sobre. También permite autenticar atributos arbitrarios, como el tiempo de firma, junto con el contenido de un mensaje. Además, proporciona otros atributos, como [*Contrafirmas*](../secgloss/c-gly.md), que se van a asociar a una firma.

El tipo de datos contenido en un \# mensaje PKCS 7 se denomina tipo de contenido. Hay dos clases de tipos de contenido: base y mejorada.

-   Los tipos de contenido base solo contienen datos sin mejoras criptográficas. Actualmente solo hay un tipo de contenido en esta clase, el [*tipo de contenido*](../secgloss/d-gly.md)de los datos.
-   Los [*tipos de contenido mejorados*](../secgloss/e-gly.md) contienen datos de algún tipo (posiblemente cifrado) y otras mejoras criptográficas (como los valores hash o las firmas).

El contenido de la clase mejorada emplea encapsulación, lo que da lugar a los términos de [*contenido externo*](../secgloss/o-gly.md) (el que contiene las mejoras) y el [*contenido interno*](../secgloss/i-gly.md) (el que se mejora). Por ejemplo, una clase mejorada podría contener el [*tipo de contenido de datos*](../secgloss/d-gly.md) (clase base) que tiene una firma incluida. En este caso, el tipo de contenido de datos es el *contenido interno* y la combinación del tipo de contenido de datos y la firma forman el contenido externo.

Los tipos de contenido definidos en el \# estándar PKCS 7 son los siguientes.



| Tipo de contenido              | Descripción                                                                                                                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data                      | Cadena de octeto (**byte**).                                                                                                                                                                                                                                                                                           |
| Datos firmados               | Contenido de cualquier tipo y [*hash*](../secgloss/h-gly.md) de mensaje cifrado ([*resúmenes*](../secgloss/m-gly.md)) del contenido para cero o más firmantes.                                                                           |
| Datos con doble cifrado            | Contenido cifrado de cualquier tipo y claves cifradas de cifrado de contenido de uno o más destinatarios. La combinación de contenido cifrado y la clave de cifrado de contenido cifrada para un destinatario es una [*envoltura digital*](../secgloss/d-gly.md) para ese destinatario. |
| Datos con signo y con doble cifrado | Contenido cifrado de cualquier tipo, claves cifradas de cifrado de contenido para uno o más destinatarios y síntesis de mensajes de cifrado doble para uno o más firmantes. El cifrado doble consta de un cifrado con la clave privada de un firmante seguido de un cifrado con la clave de cifrado de contenido.                     |
| Datos de síntesis             | Contenido de cualquier tipo y un [*hash*](../secgloss/h-gly.md) de mensaje (síntesis) del contenido.                                                                                                                                                                                             |
| Datos cifrados            | Contenido cifrado de cualquier tipo. A diferencia del [*tipo de contenido de datos*](../secgloss/d-gly.md)con doble cifrado, el tipo de contenido de datos cifrados no tiene ni destinatarios ni claves cifradas de cifrado de contenido. Se supone que las claves se administran por otros medios.               |



 

> [!Note]  
> A lo largo de la \# especificación PKCS 7, los términos *Resumen* y [*síntesis*](../secgloss/d-gly.md) hacen referencia al valor generado al aplicar un [*algoritmo hash*](../secgloss/h-gly.md) a los datos. En esta documentación se usan los términos [*hash*](../secgloss/h-gly.md) y *Hashed* para el mismo propósito. Por ejemplo, el tipo de datos utilizado con las [*funciones de mensaje de bajo nivel*](../secgloss/l-gly.md) se denomina Hashed en lugar de Digest. Para los fines de esta documentación, los dos conjuntos de términos se pueden usar indistintamente.

 

 

 
