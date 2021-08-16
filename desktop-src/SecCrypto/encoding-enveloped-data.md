---
description: La sintaxis de mensajes criptográficos se puede usar para codificar mensajes sobres.
ms.assetid: f35aacda-6827-42e9-b7ac-58dc007fc697
title: Codificación de datos con sobres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3517a956311373d067072899ee71bcdf742990877c7d569bfe4e5ef7f2757e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766770"
---
# <a name="encoding-enveloped-data"></a>Codificación de datos con sobres

Los datos sobres constan de contenido cifrado de cualquier tipo y claves de sesión de cifrado de contenido cifradas para uno o varios destinatarios. Los mensajes con sobre mantienen el contenido del secreto del mensaje y permiten que solo las personas o entidades especificadas recuperen el contenido.

La sintaxis de mensajes criptográficos (CMS) se puede usar para codificar mensajes sobres. CMS admite tres técnicas de administración de claves: transporte de claves, contrato de claves y claves de cifrado de claves simétricas (KEK) distribuidas previamente. La KEK simétrica distribuida anteriormente también se conoce como distribución de claves de lista de distribución de correo.

En cada una de estas tres técnicas, se genera una clave de sesión única para cifrar el mensaje en sobre. Los problemas de administración de claves tratan la manera en que el remitente cifra esa clave de sesión y la descifra un receptor. Un único mensaje cifrado se puede distribuir a muchos destinatarios mediante una combinación de las técnicas de administración de claves.

La administración de claves de transporte de claves usa la clave pública de un receptor previsto para cifrar la clave de sesión. El receptor descifra la clave de sesión mediante la clave privada asociada a la clave pública que se usó para cifrar. A continuación, el receptor usa la clave de sesión descifrada para descifrar los datos sobreados. Cuando se usa el transporte de claves, el receptor no ha confirmado información sobre la identidad del remitente.

En la administración de contratos de claves, se genera una clave Diffie-Hellman clave privada temporal y se usa para cifrar la clave de sesión. La clave pública correspondiente a la clave privada efímera se incluye como parte de la información del destinatario del mensaje. El destinatario descifra la clave de sesión mediante la clave efímera recibida y usa esta clave de sesión descifrada para descifrar el mensaje sobres. Mediante el acuerdo de clave efímera junto con la clave privada del receptor, el receptor del mensaje tiene información confirmada sobre la identidad del remitente.

Para la administración de [](../secgloss/s-gly.md)claves mediante claves simétricas distribuidas previamente, cada mensaje incluye la clave de cifrado de contenido que se ha cifrado con una clave de cifrado de claves distribuida previamente. Los receptores usan la clave de cifrado de claves distribuida previamente para descifrar la clave de cifrado de contenido y, a continuación, usan la clave de cifrado de contenido descifrada para descifrar el mensaje envoltorio.

En la ilustración siguiente se muestra una secuencia típica de eventos de CMS para codificar datos sobreados.

![codificación de datos envolventes](images/envelmsg.png)

-   Se recupera un [*puntero*](../secgloss/p-gly.md) al mensaje de texto no cifrado.
-   Se genera una [*clave simétrica (sesión).*](../secgloss/s-gly.md)
-   La [*clave simétrica y*](../secgloss/s-gly.md) el algoritmo de cifrado especificado se usan para cifrar los datos del mensaje.
-   Se [*abre un almacén*](../secgloss/c-gly.md) de certificados.
-   El certificado del destinatario se recupera del almacén.
-   La [*clave pública*](../secgloss/p-gly.md) se recupera del certificado del destinatario.
-   Con la clave pública del destinatario, se cifra la clave simétrica.
-   Desde el certificado del destinatario, se recupera el identificador del destinatario.
-   La siguiente información se incluye en el mensaje con sobre digital: el algoritmo de cifrado de datos, los datos cifrados, la clave simétrica cifrada y la estructura de información del destinatario.

Para usar funciones de mensaje de bajo nivel para realizar las tareas típicas que se enumeran, use el procedimiento siguiente.

**Para codificar un mensaje sobre**

1.  Cree o recupere el contenido.
2.  Obtener un proveedor de servicios criptográficos.
3.  Obtenga un certificado de destinatario.
4.  Inicialice [**la estructura \_ CMSG ENVELOPED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info)
5.  Llame [**a CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del blob del mensaje codificado. Asigne memoria para ella.
6.  Llame a [**CryptMsgOpenToEncode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)pase CMSG ENVELOPED para dwMsgType y un puntero \_ a [**CMSG \_ ENVELOPED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_enveloped_encode_info) para  *pvMsgEncodeInfo*. Como resultado de esta llamada, recibirá un identificador para el mensaje abierto.
7.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 6 y un puntero a los datos que se va a cifrar, envolviendo y codificando. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
8.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 6 y los tipos de parámetro adecuados para tener acceso a los datos codificados deseados. Por ejemplo, pase CMSG CONTENT PARAM para \_ obtener un puntero a todo el mensaje \_ PKCS \# 7.

    Si el resultado de esta codificación [](../secgloss/i-gly.md) se va a usar como los datos internos de otro mensaje codificado, como un mensaje con sobres, se debe pasar el parámetro DE CMSG \_ BARE CONTENT \_ \_ PARAM. Para obtener un ejemplo, vea [Código alternativo para codificar un mensaje sobres](alternate-code-for-encoding-an-enveloped-message.md).

9.  Cierre el mensaje mediante una llamada [**a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado [](../secgloss/s-gly.md) que contiene los datos cifrados, la clave simétrica cifrada con las claves públicas del destinatario y las estructuras de datos de información del destinatario. La combinación de contenido cifrado y una clave simétrica cifrada para un destinatario es un [*sobre digital*](../secgloss/d-gly.md) para ese destinatario. Cualquier tipo de contenido se puede envoltorio para varios destinatarios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programa C de ejemplo: codificación de un mensaje con sobres firmado](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
