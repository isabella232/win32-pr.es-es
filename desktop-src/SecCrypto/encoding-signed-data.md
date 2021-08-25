---
description: Muestra el procedimiento para codificar un mensaje firmado.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codificación de datos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e5c3ab338c4e7b251416f1a488747eb0c9b897c1fa02082afcb580cb12341b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874854"
---
# <a name="encoding-signed-data"></a>Codificación de datos firmados

[*Los datos firmados*](../secgloss/s-gly.md) constan de contenido de cualquier tipo y hash de mensajes [*cifrados*](../secgloss/h-gly.md) del contenido por cero o más firmantes. El hash resultante puede confirmar que el mensaje original no se ha modificado desde la firma y que determinadas personas o entidades firmaron los datos.

En la ilustración siguiente se muestra el procedimiento para codificar un mensaje firmado. En la lista que sigue a la ilustración se describen los pasos.

Un mensaje puede tener varios firmantes, algoritmos hash y certificados. Aunque en la ilustración solo se muestran los certificados, [*las CRL*](../secgloss/c-gly.md)y [*las CL*](../secgloss/c-gly.md) pueden usar el mismo proceso. Caben en la ilustración dondequiera que se muestran los certificados.

![codificación de un mensaje firmado](images/signmsg2.png)

El proceso general para codificar [*datos firmados*](../secgloss/s-gly.md) es el siguiente.

**Para codificar datos firmados**

1.  Los datos se crean (si es necesario) y se recupera un puntero a los datos.
2.  Se [*abre un almacén*](../secgloss/c-gly.md) de certificados que contiene el certificado del firmante.
3.  Se recupera la clave privada del certificado. Hay dos propiedades que se deben establecer en el certificado antes de usarlo. Uno se usa para vincular un certificado a un CSP determinado y, dentro de ese CSP, a un contenedor de [*claves privadas determinado.*](../secgloss/k-gly.md) El otro se usa para indicar qué algoritmo hash se va a usar cuando se llama a una operación [*hash.*](../secgloss/h-gly.md) Solo se deben establecer una vez.
4.  La propiedad de un certificado determina el algoritmo hash.
5.  Se crea un hash de los datos mediante el envío de los datos a través de la función hash.
6.  La firma se crea mediante el cifrado del hash mediante la clave privada, obtenida a través de una propiedad en el certificado.
7.  Los datos siguientes se incluyen en el mensaje firmado finalizado:
    -   Los datos originales que se firmarán
    -   Algoritmos hash
    -   Las firmas
    -   Las estructuras de información del firmante, que incluyen el identificador del firmante (emisor de certificado y número de serie)
    -   Certificados del firmante (opcional)

En este procedimiento se muestra un caso sencillo. Los casos más complejos implican atributos autenticados incluidos en el mensaje. Cuando el tipo de contenido es cualquier cosa menos una cadena **BYTE,** o hay al menos un atributo autenticado junto con cualquier tipo de datos, se requieren dos atributos autenticados estándar: el tipo de contenido (datos) y el hash del contenido. En estas circunstancias, [*CryptoAPI*](../secgloss/c-gly.md) proporciona automáticamente estos dos atributos necesarios. Las funciones de mensaje de bajo nivel aplica un algoritmo hash a los atributos autenticados, cifran el hash con la clave privada y lo proporcionan como firma.

Use las funciones de mensaje de bajo nivel para realizar las tareas que acaba de enumerar, mediante el procedimiento siguiente.

**Para codificar un mensaje firmado**

1.  Cree o recupere el contenido.
2.  Obtener un proveedor de servicios criptográficos.
3.  Obtenga los certificados de firmante.
4.  Inicialice [**la estructura \_ CMSG SIGNER \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info)
5.  Inicialice [**la estructura \_ CMSG SIGNED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info)
6.  Llame [**a CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del blob del mensaje codificado. Asigne memoria para él.
7.  Llame a [**CryptMsgOpenToEncode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)pasando CMSG SIGNED para dwMsgType y un puntero \_ a [**CMSG \_ SIGNED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) para *pvMsgEncodeInfo* para obtener un identificador al mensaje abierto. 
8.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 7 y un puntero a los datos que se firmarán y codificarán. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
9.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 7 y los tipos de parámetro adecuados para acceder a los datos codificados deseados. Por ejemplo, pase CMSG CONTENT PARAM para \_ obtener un puntero a todo el mensaje \_ [*PKCS \# 7.*](../secgloss/p-gly.md)

    Si el resultado de esta codificación [](../secgloss/i-gly.md) se va a usar como datos internos para otro mensaje codificado, como un mensaje con sobres, se debe pasar el parámetro CMSG \_ BARE CONTENT \_ \_ PARAM. Para obtener un ejemplo en el que se muestra esto, vea [Código alternativo para codificar un mensaje con sobres](alternate-code-for-encoding-an-enveloped-message.md).

10. Cierre el mensaje mediante una [**llamada a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado que contiene los datos originales, el hash cifrado de los datos (firma) y la información del firmante. También hay un puntero al BLOB codificado deseado.

Para obtener detalles de codificación de C, vea [Programa de C de ejemplo: firma, codificación, codificación](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)y comprobación de un mensaje .

 

 
