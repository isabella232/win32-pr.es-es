---
description: Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticación de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277146"
---
# <a name="key-authentication"></a>Autenticación de clave

Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.

Las técnicas de autenticación que se basan en un secreto, como una contraseña, deben tener una manera de evitar que el secreto se convierta en un conocimiento público. Un propietario de contraseña no puede recorrer una puerta y proporcionar la contraseña. Es posible que alguien además del Doorkeeper esté escuchando; o bien, podría ser la puerta equivocada. Con el fin de mantener un secreto, debe haber una manera de demostrar que un usuario conoce la contraseña sin revelar la contraseña. Esta es la idea detrás de la autenticación de clave secreta, un método de comprobación utilizado en el [*protocolo Kerberos*](../secgloss/k-gly.md).

Tenga en cuenta que el "secreto" en la autenticación de clave secreta es que el proceso de autenticación tiene lugar "en secreto", es decir, sin revelar realmente el contenido de la clave.

Para que la autenticación de clave secreta funcione, las dos partes de una transacción deben compartir una [*clave de sesión*](../secgloss/s-gly.md) criptográfica, que también es secreta, solo las conoce y no otras. La clave es [*simétrica*](../secgloss/s-gly.md); es decir, es una clave única que se usa para el cifrado y el descifrado. Una parte del proceso de autenticación demuestra su conocimiento de la clave mediante el cifrado de un mensaje. La otra parte demuestra su conocimiento de la clave mediante el descifrado del mensaje.

 

 
