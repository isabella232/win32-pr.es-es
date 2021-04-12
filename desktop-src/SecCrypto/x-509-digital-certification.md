---
description: La certificación digital implica un proceso para firmar el certificado. Este proceso se describe.
ms.assetid: bb0382fd-2924-429f-933b-84ab61debf20
title: Certificación digital X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2f737a658e3e2c44876a23206f23a3d45ff3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277001"
---
# <a name="x509-digital-certification"></a>Certificación digital X.509

Una tarea principal de un [*certificado digital*](../secgloss/d-gly.md) es proporcionar acceso a la [*clave pública*](../secgloss/p-gly.md)del sujeto. El certificado también confirma que la clave pública del certificado pertenece al sujeto del certificado. Por ejemplo, una [*entidad de certificación*](../secgloss/c-gly.md) (CA) puede firmar digitalmente un mensaje especial (la información de certificado) que contiene el nombre de algún usuario, por ejemplo, "Alice", y su clave pública. Esto se debe hacer de tal forma que cualquiera pueda comprobar que el certificado se ha emitido y firmado por no una entidad de certificación. Si la CA es de confianza y se puede comprobar que el certificado de Alice fue emitido por esa CA, cualquier receptor del certificado de Alice puede confiar en la clave pública de Alice de ese certificado.

La implementación típica de la certificación digital implica un proceso para firmar el certificado.

El proceso es similar al siguiente:

1.  Alice envía una [*solicitud de certificado*](../secgloss/c-gly.md) firmada que contiene su nombre, su clave pública y quizás alguna información adicional a una CA.
2.  La CA crea un mensaje, *m*, a partir de la solicitud de Alice. La CA firma el mensaje con su clave privada y crea un mensaje de firma independiente, *SIG*. La CA devuelve el mensaje, *m* y la firma, *SIG*, a Alice. Juntos, el certificado de Alice del formulario *m* y *SIG* .
3.  Alice envía dos partes de su certificado a Bob para concederle acceso a su clave pública.
4.  Bob comprueba la firma, *SIG* mediante la clave pública de la CA. Si la firma es válida, acepta la clave pública en el certificado como la clave pública de Alice.

Como con cualquier [*firma digital*](../secgloss/d-gly.md), cualquier receptor con acceso a la clave pública de la CA puede determinar si una entidad de certificación específica firmó el certificado. Este proceso no requiere acceso a ninguna información secreta. El escenario que se acaba de presentar supone que Bob tiene acceso a la clave pública de la CA. Bob tendría acceso a esa clave si tiene una copia del certificado de la CA que contiene esa clave pública.

Los certificados digitales [*X. 509*](../secgloss/x-gly.md) incluyen no solo el nombre y la clave pública de un usuario, sino también otra información sobre el usuario. Estos certificados son más que las piedras de paso en una jerarquía de confianza digital. Permiten a la entidad de certificación proporcionar al receptor de un certificado un medio de confiar no solo en la clave pública del sujeto del certificado, sino también en otra información sobre el sujeto del certificado. Esta información puede incluir, entre otras cosas, una dirección de correo electrónico, una autorización para firmar documentos de un valor determinado o la autorización para convertirse en CA y firmar otros certificados.

Los certificados X. 509 y muchos otros certificados tienen una duración de tiempo válida. Un certificado puede expirar y ya no es válido. Una entidad de certificación puede revocar un certificado por una serie de motivos. Para controlar las revocación, una CA mantiene y distribuye una lista de certificados revocados denominada [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL). Los usuarios de la red tienen acceso a la CRL para determinar la validez de un certificado.

 

 
