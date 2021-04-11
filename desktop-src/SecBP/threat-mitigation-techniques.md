---
description: Hay una serie de técnicas de mitigación de amenazas disponibles que puede usar para proteger las contraseñas mejor.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Técnicas de mitigación de amenazas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ec2b8db3a634ea93ce77d585038909056c7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912418"
---
# <a name="threat-mitigation-techniques"></a>Técnicas de mitigación de amenazas

Hay una serie de técnicas de mitigación de amenazas disponibles que puede usar para proteger las contraseñas mejor. Estas técnicas se implementan mediante el uso de una o varias de las siguientes cuatro tecnologías principales.



| Technology                      | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | CryptoAPI proporciona un conjunto de funciones que le ayudan a aplicar rutinas criptográficas a entidades de destino. CryptoAPI puede proporcionar valores hash, resúmenes, cifrado y descifrado para mencionar su funcionalidad principal. CryptoAPI también tiene otras características. Para obtener información sobre la criptografía y la CryptoAPI, consulte [Criptografía Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Listas de control de acceso            | Una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) es una lista de protecciones de seguridad que se aplica a un objeto. Un objeto puede ser un archivo, un proceso, un evento o cualquier otro elemento que tenga un descriptor de seguridad. Para obtener más información acerca de [las](/windows/desktop/SecAuthZ/access-control-lists) ACL, consulte listas de Access Control (ACL). |
| API de protección de datos             | La API de protección de datos (DPAPI) proporciona las cuatro funciones siguientes que se utilizan para cifrar y descifrar datos confidenciales: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)y [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Nombres de usuario y contraseñas almacenados | Funcionalidad de almacenamiento que permite administrar las contraseñas de los usuarios y otras credenciales, como las claves privadas, más fáciles, coherentes y seguras. Para obtener más información sobre esta funcionalidad, vea [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).                                                                                                         |



 

Estas tecnologías no están disponibles en todos los sistemas operativos. Por lo tanto, la medida en la que se puede mejorar la seguridad depende de los sistemas operativos que intervienen. Estas son las tecnologías disponibles en cada sistema operativo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Technology</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Server 2003 y Windows XP</td>
<td><ul>
<li>CryptoAPI</li>
<li>Listas de control de acceso</li>
<li>API de protección de datos</li>
<li>Nombres de usuario y contraseñas almacenados</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 2000</td>
<td><ul>
<li>CryptoAPI</li>
<li>Listas de control de acceso</li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Las siguientes técnicas de mitigación de amenazas usan una o varias de las cuatro tecnologías. No se pueden usar técnicas que requieran el uso de tecnologías que no están incluidas en el sistema operativo.

## <a name="getting-passwords-from-the-user"></a>Obtención de contraseñas del usuario

Cuando permite al usuario configurar una contraseña, fuerce el uso de contraseñas seguras. Por ejemplo, exija que las contraseñas tengan una longitud mínima, como ocho caracteres o más. También es necesario que las contraseñas incluyan letras mayúsculas y minúsculas, números y otros caracteres del teclado como el signo de dólar ($), el signo de exclamación (!) o mayor que (>).

Después de obtener una contraseña, úsela rápidamente (usando el menor código posible) y, a continuación, borre todos los Vestiges de la contraseña. Esto minimiza el tiempo disponible para que un intruso "Capture" la contraseña. El equilibrio con esta técnica es la frecuencia con la que se debe recuperar la contraseña del usuario; sin embargo, el principio se debe emplear siempre que sea posible. Para obtener información sobre cómo obtener correctamente las contraseñas, consulte [solicitar credenciales al usuario](asking-the-user-for-credentials.md).

Evite proporcionar las opciones de la interfaz de usuario "recordar mi contraseña". A menudo, los usuarios solicitarán esta opción. Si debe proporcionarla, como mínimo, asegúrese de que la contraseña se guarda de manera segura. Para obtener más información, vea la sección almacenar contraseñas, más adelante en este tema.

Limitar los intentos de entrada de contraseña. Después de un número determinado de intentos sin éxito, bloquee al usuario durante un período de tiempo determinado. Opcionalmente, prolongar el tiempo de respuesta para cada intento en un máximo. Esta técnica está destinada a derrotar un ataque de adivinación.

## <a name="storing-passwords"></a>Almacenar contraseñas

Nunca almacene las contraseñas en texto sin formato (sin cifrar). El cifrado de contraseñas aumenta significativamente la seguridad. Para obtener información sobre el almacenamiento de contraseñas cifradas, consulte [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Para obtener información sobre el cifrado de contraseñas en memoria, vea [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Almacene las contraseñas en el menor número de veces posible. Cuanto más lugares se almacena una contraseña, mayor será la probabilidad de que un intruso pueda encontrarla. Nunca almacene las contraseñas en una página web o en un archivo basado en Web. Almacenar contraseñas en una página web o en un archivo basado en web permite que se pongan en peligro fácilmente.

Una vez que haya cifrado una contraseña y lo haya almacenado, use ACL seguras para limitar el acceso al archivo. Como alternativa, puede almacenar contraseñas y claves de cifrado en dispositivos extraíbles. El almacenamiento de contraseñas y claves de cifrado en un medio extraíble, como una tarjeta inteligente, le ayuda a crear un sistema más seguro. Una vez recuperada una contraseña para una sesión determinada, la tarjeta se puede quitar, con lo que se elimina la posibilidad de que un intruso pueda obtener acceso a ella.

 

 
