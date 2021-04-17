---
description: Todas las operaciones normales de RSA/Schannel y Diffie-Hellman/Schannel usan el \_ par de claves pública y privada de KEYEXCHANGE.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Uso del par de claves pública y privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688037"
---
# <a name="publicprivate-key-pair-usage"></a>Uso del par de claves pública y privada

Todas las operaciones normales de [*RSA*](../secgloss/r-gly.md)/Schannel y [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel usan \_ el [*par de claves pública y privada*](../secgloss/p-gly.md)de KEYEXCHANGE. Para proporcionar [*autenticación*](../secgloss/a-gly.md)de servidor, el servidor de las operaciones Schannel debe tener acceso a su certificado [*X. 509*](../secgloss/x-gly.md) que contiene su clave pública y tener acceso a la [*clave privada*](../secgloss/p-gly.md)correspondiente. El lado cliente de [*Schannel*](../secgloss/s-gly.md) necesita su certificado con su clave pública y acceso a su clave privada si se implementa la autenticación del cliente.

Dado que los motores de protocolo Schannel nunca usan el \_ par de claves pública y privada de la firma, ese par de claves no es compatible con un nuevo CSP que solo admite RSA/Schannel o Diffie-Hellman/Schannel.

Si un motor de protocolo usa un conjunto de cifrado de exportación SSL 3,0 con un \_ par de claves at KEYEXCHANGE superior a 512 bits, el servidor debe utilizar un par de claves RSA adicional. Este par de claves adicional siempre es exactamente 512 bits y puede ser efímero. El par se almacena como un \_ elemento en KEYEXCHANGE en un contenedor de claves propiedad del motor de protocolo. Un identificador de este contenedor de claves se adquiere normalmente en el inicio del motor de protocolo.

Diffie-Hellman solo admite [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) y usa claves públicas RSA o DSS normales.

 

 
