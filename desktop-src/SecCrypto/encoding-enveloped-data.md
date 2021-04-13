---
description: Se puede usar la sintaxis de mensajes criptográficos para codificar mensajes con doble cifrado.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codificación de datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dc20fc7483ba1ef364d8b59824d26bd14d458d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559449"
---
# <a name="encoding-enveloped-data"></a>Codificación de datos con doble cifrado

Los datos con doble cifrado se componen de contenido cifrado de cualquier tipo y claves de sesión cifradas de cifrado de contenido para uno o más destinatarios. Los mensajes con doble cifrado mantienen el contenido del mensaje secreto y permiten que solo las personas o entidades especificadas recuperen el contenido.

La sintaxis de mensajes criptográficos (CMS) se puede usar para codificar mensajes con doble cifrado. CMS admite tres técnicas de administración de claves: transporte de claves, contrato de claves y claves de cifrado de claves simétricas (KEK) distribuidas previamente. Los KEK simétricos distribuidos previamente también se conocen como distribución de claves de lista de distribución de correo.

En cada una de estas tres técnicas, se genera una clave de sesión única para cifrar el mensaje con doble cifrado. Los problemas de administración de claves solucionan la manera en que el remitente cifra la clave de sesión y la descifra un receptor. Un solo mensaje cifrado se puede distribuir a muchos destinatarios mediante una combinación de las técnicas de administración de claves.

La administración de claves de transporte de claves utiliza la clave pública del receptor previsto para cifrar la clave de sesión. El receptor descifra la clave de sesión mediante la clave privada asociada a la clave pública que se usó para cifrar. A continuación, el receptor usa la clave de sesión descifrada para descifrar los datos con doble cifrado. Cuando se utiliza el transporte de claves, el receptor no ha confirmado la información sobre la identidad del remitente.

En la administración de acuerdos de claves, se genera una clave privada Diffie-Hellman temporal y efímera que se usa para cifrar la clave de sesión. La clave pública correspondiente a la clave privada efímera se incluye como parte de la información del destinatario del mensaje. El destinatario descifra la clave de sesión mediante la clave efímera recibida y usa esta clave de sesión descifrada para descifrar el mensaje con doble cifrado. Mediante el uso del acuerdo de claves efímeras junto con la clave privada del receptor, el receptor del mensaje ha confirmado la información sobre la identidad del remitente.

Para la administración de claves mediante [*claves simétricas*](../secgloss/s-gly.md)distribuidas previamente, cada mensaje incluye la clave de cifrado de contenido que se ha cifrado con una clave de cifrado de clave distribuida previamente. Los receptores usan la clave de cifrado de clave distribuida previamente para descifrar la clave de cifrado de contenido y, a continuación, usan la clave de cifrado de contenido descifrado para descifrar el mensaje con doble cifrado.

En la ilustración siguiente se muestra una secuencia CMS típica de eventos para codificar los datos con doble cifrado.

![codificación de datos con doble cifrado](images/envelmsg.png)

-   Se recupera un puntero al mensaje de [*texto simple*](../secgloss/p-gly.md) .
-   Se genera una clave simétrica ([*sesión*](../secgloss/s-gly.md)).
-   La [*clave simétrica*](../secgloss/s-gly.md) y el algoritmo de cifrado especificado se utilizan para cifrar los datos del mensaje.
-   Se abre un [*almacén de certificados*](../secgloss/c-gly.md) .
-   El certificado del destinatario se recupera del almacén.
-   La [*clave pública*](../secgloss/p-gly.md) se recupera del certificado del destinatario.
-   Con la clave pública del destinatario, la clave simétrica está cifrada.
-   En el certificado del destinatario, se recupera el identificador del destinatario.
-   La siguiente información se incluye en el mensaje con sobre digital: el algoritmo de cifrado de datos, los datos cifrados, la clave simétrica cifrada y la estructura de información del destinatario.

Para usar funciones de mensaje de bajo nivel para realizar las tareas típicas que se acaban de mostrar, use el procedimiento siguiente.

**Para codificar un mensaje con doble cifrado**

1.  Cree o recupere el contenido.
2.  Obtener un proveedor de servicios criptográficos.
3.  Obtener un certificado de destinatario.
4.  Inicializa la estructura de [**\_ información de \_ codificación \_ con doble cifrado de CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) .
5.  Llame a [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del BLOB del mensaje codificado. Asigne memoria.
6.  Llame a [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), pasando CMSG \_ sobre *dwMsgType* y un puntero a la información de [**\_ \_ codificación \_ con doble cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) para *pvMsgEncodeInfo*. Como resultado de esta llamada, obtendrá un identificador para el mensaje abierto.
7.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 6 y un puntero a los datos que se van a cifrar, sobre y codificar. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
8.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 6 y los tipos de parámetro adecuados para tener acceso a los datos codificados deseados. Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al mensaje PKCS \# 7 completo.

    Si el resultado de esta codificación se va a usar como [*datos internos*](../secgloss/i-gly.md) de otro mensaje codificado, como un mensaje con doble cifrado, \_ \_ \_ se debe pasar el parámetro de parámetro CMSG de código sin sistema operativo. Para obtener un ejemplo, vea [código alternativo para codificar un mensaje con doble cifrado](alternate-code-for-encoding-an-enveloped-message.md).

9.  Cierre el mensaje mediante una llamada a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado que contiene los datos cifrados, la [*clave simétrica*](../secgloss/s-gly.md) cifrada con las claves públicas del destinatario y las estructuras de datos de información de destinatarios. La combinación de contenido cifrado y una clave simétrica cifrada para un destinatario es una [*envoltura digital*](../secgloss/d-gly.md) para ese destinatario. Se puede hacer sobre cualquier tipo de contenido para varios destinatarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programa C de ejemplo: codificar un mensaje con signo de cifrado](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
