---
description: Tareas generales necesarias para descodificar un mensaje con doble cifrado.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Descodificar datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550422"
---
# <a name="decoding-enveloped-data"></a>Descodificar datos con doble cifrado

Las tareas generales necesarias para descodificar un mensaje con doble cifrado se muestran en la siguiente ilustración y se describen en la lista que lo sigue.

![descodificar datos con doble cifrado](images/decemsg.png)

La secuencia de eventos para descodificar los datos con sobres mediante la administración de claves de transporte de claves, como se describe en la ilustración anterior, es la siguiente:

-   Se recupera un puntero al mensaje con [*doble cifrado*](../secgloss/d-gly.md) .
-   Se abre un [*almacén de certificados*](../secgloss/c-gly.md) .
-   En el mensaje, se recupera el identificador del destinatario (My ID).
-   El identificador de destinatario se usa para recuperar el certificado.
-   Se recupera la [*clave privada*](../secgloss/p-gly.md) asociada a ese certificado.
-   La clave privada se usa para descifrar la clave [*simétrica*](../secgloss/s-gly.md) ([*sesión*](../secgloss/s-gly.md)).
-   El algoritmo de cifrado se recupera del mensaje.
-   Con la clave privada y el algoritmo de cifrado, se descifran los datos.

En el procedimiento siguiente se usan funciones de mensaje de bajo nivel para realizar las tareas que se acaban de mostrar.

**Para descodificar un mensaje con doble cifrado**

1.  Obtiene un puntero al objeto binario codificado.
2.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se van a descodificar. Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 2 y el \_ \_ parámetro de tipo CMSG para comprobar que el mensaje es del tipo de datos con doble cifrado.
5.  Vuelva a llamar a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando \_ CMSG \_ parámetro de tipo de contenido interno \_ \_ para obtener el tipo de datos del [*contenido interno*](../secgloss/i-gly.md).
6.  Si el tipo de datos de contenido interno son **datos**, continúe para descifrar y descodificar el contenido. De lo contrario, ejecute un procedimiento de descodificación apropiado para el tipo de datos de contenido.
7.  Suponiendo que el tipo de contenido interno sea "Data", inicialice [**CMSG \_ Ctrl \_ descrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) la estructura de datos y llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando el \_ \_ descifrado de CMSG Ctrl y la dirección de la estructura. El contenido se descifrará.
8.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando \_ el parámetro de contenido CMSG \_ para obtener un puntero al objeto binario de datos de contenido descodificado (cadena de **bytes** ).
9.  Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

El resultado de este procedimiento es que el mensaje se descodifica y se descifra y se recupera un puntero al BLOB de datos de contenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programa C de ejemplo: codificar un mensaje con signo de cifrado](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
