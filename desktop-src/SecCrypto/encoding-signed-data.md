---
description: Describe el procedimiento para codificar un mensaje firmado.
ms.assetid: 40d1c417-6d88-4421-920f-8b40d88d28ce
title: Codificar datos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4a542fe0890a6ee9d51ebc1a5ee6b98bab4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278239"
---
# <a name="encoding-signed-data"></a>Codificar datos firmados

Los [*datos firmados*](../secgloss/s-gly.md) constan de contenido de cualquier tipo y [*hash*](../secgloss/h-gly.md) de mensaje cifrado del contenido por cero o más firmantes. El hash resultante puede confirmar que el mensaje original no se ha modificado desde la firma y que determinadas personas o entidades firmaron los datos.

En la ilustración siguiente se muestra el procedimiento para codificar un mensaje firmado. En la lista siguiente se describen los pasos.

Un mensaje puede tener varios firmadores, algoritmos hash y certificados. Mientras que la ilustración solo muestra certificados, [*CRL*](../secgloss/c-gly.md)y [*CTL*](../secgloss/c-gly.md) , puede usar el mismo proceso. Caben en la ilustración siempre que se muestren los certificados.

![codificar un mensaje firmado](images/signmsg2.png)

El proceso general para codificar los [*datos firmados*](../secgloss/s-gly.md) es el siguiente.

**Para codificar datos firmados**

1.  Los datos se crean (si es necesario) y se recupera un puntero a él.
2.  Se abre un [*almacén de certificados*](../secgloss/c-gly.md) que contiene el certificado del firmante.
3.  Se recupera la clave privada para el certificado. Hay dos propiedades que se deben establecer en el certificado antes de usarlas. Una se usa para asociar un certificado a un CSP determinado y, dentro de ese CSP, a un [*contenedor de claves*](../secgloss/k-gly.md)privadas determinado. El otro se usa para indicar qué algoritmo hash se va a utilizar cuando se llama a una operación [*hash*](../secgloss/h-gly.md) . Solo se deben establecer una vez.
4.  La propiedad de un certificado determina el algoritmo hash.
5.  Un hash de los datos se crea mediante el envío de los datos a través de la función hash.
6.  La firma se crea mediante el cifrado del hash mediante la clave privada, obtenida a través de una propiedad en el certificado.
7.  Los datos siguientes se incluyen en el mensaje finalizado firmado:
    -   Los datos originales que se van a firmar.
    -   Algoritmos hash
    -   Las firmas
    -   Las estructuras de información del firmante, que incluye el identificador del firmante (emisor de certificados y número de serie)
    -   Los certificados del firmante (opcional)

En este procedimiento se ilustra un caso sencillo. Los casos más complejos implican atributos autenticados incluidos en el mensaje. Cuando el tipo de contenido es cualquier cosa excepto una cadena de **bytes** , o hay al menos un atributo autenticado junto con cualquier tipo de datos, se requieren dos atributos estándar autenticados: el tipo de contenido (datos) y el hash del contenido. En estas circunstancias, [*CryptoAPI*](../secgloss/c-gly.md) proporciona automáticamente estos dos atributos necesarios. Las funciones de mensaje de bajo nivel aplican un algoritmo hash a los atributos autenticados, cifran el hash con la clave privada y lo proporcionan como firma.

Utilice las funciones de mensaje de bajo nivel para realizar las tareas que se acaban de enumerar mediante el procedimiento siguiente.

**Para codificar un mensaje firmado**

1.  Cree o recupere el contenido.
2.  Obtener un proveedor de servicios criptográficos.
3.  Obtener los certificados del firmante.
4.  Inicializa la estructura de [**\_ \_ \_ información de codificador de CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) .
5.  Inicialice la estructura de [**\_ \_ \_ información de codificación firmada CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
6.  Llame a [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del BLOB del mensaje codificado. Asigne memoria.
7.  Llame a [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), pasando CMSG \_ signed para *dwMsgType* y un puntero a [**CMSG \_ \_ \_ información de codificación firmada**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) para *pvMsgEncodeInfo* para obtener un identificador del mensaje abierto.
8.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 7 y un puntero a los datos que se van a firmar y codificar. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
9.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 7 y los tipos de parámetro adecuados para tener acceso a los datos codificados deseados. Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al mensaje [*PKCS \# 7*](../secgloss/p-gly.md) completo.

    Si el resultado de esta codificación se va a usar como [*datos internos*](../secgloss/i-gly.md) de otro mensaje codificado, como un mensaje con doble cifrado, \_ \_ \_ se debe pasar el parámetro de parámetro CMSG de código sin sistema operativo. Para ver un ejemplo que muestra esto, consulte el [código alternativo para codificar un mensaje con doble cifrado](alternate-code-for-encoding-an-enveloped-message.md).

10. Cierre el mensaje mediante una llamada a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado que contiene los datos originales, el hash cifrado de los datos (firma) y la información del firmante. También hay un puntero al BLOB codificado deseado.

Para obtener información detallada sobre la codificación en C, vea [ejemplo de programa c: firma, codificación, descodificación y comprobación de un mensaje](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
