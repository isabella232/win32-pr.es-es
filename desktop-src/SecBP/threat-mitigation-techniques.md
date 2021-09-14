---
description: Hay una serie de técnicas de mitigación de amenazas disponibles que puede usar para proteger mejor las contraseñas.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Técnicas de mitigación de amenazas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315a79ec1db48a16de858d655bd1550fa1458720
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253611"
---
# <a name="threat-mitigation-techniques"></a>Técnicas de mitigación de amenazas

Hay una serie de técnicas de mitigación de amenazas disponibles que puede usar para proteger mejor las contraseñas. Estas técnicas se implementan mediante una o varias de las cuatro tecnologías principales siguientes.



| Tecnología                      | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cryptoapi                       | CryptoAPI proporciona un conjunto de funciones que le ayudan a aplicar rutinas criptográficas a entidades de destino. CryptoAPI puede proporcionar hashes, resúmenes, cifrado y descifrado, por mencionar su funcionalidad principal. CryptoAPI también tiene otras características. Para obtener información sobre la criptografía y CryptoAPI, vea [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Listas de control de acceso            | Una [*lista de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACL) es una lista de protecciones de seguridad que se aplica a un objeto . Un objeto puede ser un archivo, un proceso, un evento o cualquier otra cosa que tenga un descriptor de seguridad. Para obtener más información sobre las [ACL, consulte Access Control listas de](/windows/desktop/SecAuthZ/access-control-lists) control de acceso (ACL). |
| API de protección de datos             | La API de protección de datos (DPAPI) proporciona las cuatro funciones siguientes que se usan para cifrar y descifrar datos confidenciales: [**CryptProtectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) [**CryptUnprotectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)y [**CryptUnprotectMemory.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory)                  |
| Nombres de usuario y contraseñas almacenados | Storage funcionalidad que hace que el control de las contraseñas de los usuarios y otras credenciales, como las claves privadas, sea más fácil, coherente y más seguro. Para obtener más información sobre esta funcionalidad, [**vea CredUIPromptForCredentials.**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)                                                                                                         |



 

Estas tecnologías no están disponibles en todos los sistemas operativos. Por lo tanto, la medida en que se puede mejorar la seguridad depende de qué sistemas operativos estén implicados. Estas son las tecnologías que están disponibles en cada sistema operativo.


| Sistema operativo | Tecnología | 
|------------------|------------|
| Windows Server 2003 y Windows XP | <ul><li>Cryptoapi</li><li>Listas de control de acceso</li><li>API de protección de datos</li><li>Nombres de usuario y contraseñas almacenados</li></ul> | 
| Windows 2000 | <ul><li>Cryptoapi</li><li>Listas de control de acceso</li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li></ul> | 




 

Las siguientes técnicas de mitigación de amenazas usan una o varias de las cuatro tecnologías. No se pueden usar técnicas que requieran el uso de tecnologías que no están incluidas en el sistema operativo.

## <a name="getting-passwords-from-the-user"></a>Obtención de contraseñas del usuario

Cuando permita que el usuario configure una contraseña, fuerce el uso de contraseñas seguras. Por ejemplo, requerir que las contraseñas sean de una longitud mínima, como ocho caracteres o más. Las contraseñas también deben incluir letras mayúsculas y minúsculas, números y otros caracteres de teclado, como el signo de dólar ($), el signo de exclamación (!) o mayor que (>).

Después de obtener una contraseña, úsela rápidamente (con el menos código posible) y, a continuación, borre todos los vestigios de la contraseña. Esto minimiza el tiempo disponible para que un intrusista "atrase" la contraseña. El intercambio con esta técnica es la frecuencia con la que se debe recuperar la contraseña del usuario. sin embargo, el principio debe emplearse siempre que sea posible. Para obtener información sobre cómo obtener correctamente contraseñas, vea [Asking the User for Credentials](asking-the-user-for-credentials.md).

Evite proporcionar opciones de interfaz de usuario "recordar mi contraseña". A menudo, los usuarios exigirán tener esta opción. Si debe proporcionarla, como mínimo, asegúrese de que la contraseña se guarda de forma segura. Para obtener información, vea la sección Almacenamiento de contraseñas, más adelante en este tema.

Limitar los intentos de entrada de contraseña. Después de un número determinado de intentos sin éxito, bloquee el usuario durante un período de tiempo determinado. Si lo desea, puede longitudar el tiempo de respuesta de cada prueba en un máximo. Esta técnica está dirigida a la desagresión de un ataque de suposición.

## <a name="storing-passwords"></a>Almacenamiento de contraseñas

Nunca almacene contraseñas en texto no cifrado (sin cifrar). El cifrado de contraseñas aumenta significativamente su seguridad. Para obtener información sobre cómo almacenar contraseñas cifradas, vea [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Para obtener información sobre el cifrado de contraseñas en memoria, vea [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Almacene las contraseñas en el menor número de lugares posible. Entre más lugares se almacene una contraseña, mayor será la posibilidad de que un intruso la encuentre. Nunca almacene contraseñas en una página web o en un archivo basado en web. El almacenamiento de contraseñas en una página web o en un archivo basado en web permite que se comprometan fácilmente.

Después de cifrar una contraseña y almacenarla, use ACL seguras para limitar el acceso al archivo. Como alternativa, puede almacenar contraseñas y claves de cifrado en dispositivos extraíbles. El almacenamiento de contraseñas y claves de cifrado en un medio extraíble, como una tarjeta inteligente, ayuda a crear un sistema más seguro. Después de recuperar una contraseña para una sesión determinada, se puede quitar la tarjeta, lo que elimina la posibilidad de que un intruso pueda obtener acceso a ella.

 

 
