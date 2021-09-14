---
description: Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Autenticación de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160976"
---
# <a name="key-authentication"></a>Autenticación de clave

Muchas formas de autenticación se basan en la idea de que una entidad puede demostrar su identidad si puede demostrar que conoce una clave, como una contraseña, que solo puede conocer.

Las técnicas de autenticación que se basan en un secreto, como una contraseña, deben tener una manera de evitar que el secreto se convierta en conocimiento público. Un propietario de contraseña no puede ir a una puerta y proporcionar la contraseña. Es posible que alguien que no sea el guardameta esté escuchando. o podría ser la puerta equivocada. Para mantener un secreto, debe haber una manera de demostrar que un usuario conoce la contraseña sin revelarla. Esa es la idea que hay detrás de la autenticación de clave secreta, un método de comprobación que se usa en todo el [*protocolo Kerberos.*](../secgloss/k-gly.md)

Tenga en cuenta que el "secreto" en la autenticación de clave secreta es que el proceso de autenticación tiene lugar "en secreto", es decir, sin revelar realmente el contenido de la clave.

Para que la autenticación de clave secreta funcione, [](../secgloss/s-gly.md) las dos partes de una transacción deben compartir una clave de sesión criptográfica que también sea secreta, conocida solo para ellos y para ningún otro. La clave es [*simétrica;*](../secgloss/s-gly.md) es decir, es una clave única que se usa tanto para el cifrado como para el descifrado. Una parte del proceso de autenticación demuestra su conocimiento de la clave mediante el cifrado de un mensaje. La otra parte demuestra su conocimiento de la clave descifrando el mensaje.

 

 
