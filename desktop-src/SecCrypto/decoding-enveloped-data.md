---
description: Tareas generales necesarias para descodificar un mensaje sobres.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decoding Enveloped Data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767819"
---
# <a name="decoding-enveloped-data"></a>Decoding Enveloped Data

Las tareas generales necesarias para descodificar un mensaje envoltorio se describen en la siguiente ilustración y se describen en la lista que le sigue.

![decoding envelopeding data](images/decemsg.png)

La secuencia de eventos para lacoding de datos envolventes mediante la administración de claves de transporte de claves, como se muestra en la ilustración anterior, es la siguiente:

-   Se recupera un [*puntero*](../secgloss/d-gly.md) al mensaje con sobre digital.
-   Se [*abre un almacén*](../secgloss/c-gly.md) de certificados.
-   En el mensaje, se recupera el identificador de destinatario (Mi identificador).
-   El identificador de destinatario se usa para recuperar el certificado.
-   Se [*recupera la*](../secgloss/p-gly.md) clave privada asociada a ese certificado.
-   La clave privada se usa para descifrar la [*clave simétrica*](../secgloss/s-gly.md) [*(sesión).*](../secgloss/s-gly.md)
-   El algoritmo de cifrado se recupera del mensaje.
-   Con la clave privada y el algoritmo de cifrado, los datos se descifran.

En el procedimiento siguiente se usan funciones de mensaje de bajo nivel para realizar las tareas que acaba de enumerar.

**Para descodificar un mensaje sobre**

1.  Obtenga un puntero al BLOB codificado.
2.  Llame [**a CryptMsgOpenToDecode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)pase los argumentos necesarios.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se va a descodificar. Esto hace que se tome las acciones adecuadas en el mensaje, dependiendo del tipo de mensaje.
4.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 2 y CMSG TYPE PARAM para comprobar que el mensaje es del tipo de datos \_ \_ sobreados.
5.  Vuelva a [**llamar a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)y pase CMSG INNER CONTENT TYPE PARAM para obtener el tipo de datos \_ del contenido \_ \_ \_ [*interno.*](../secgloss/i-gly.md)
6.  Si el tipo de datos de contenido interno **son datos**, continúe para descifrar y descodificar el contenido. De lo contrario, ejecute un procedimiento decoding adecuado para el tipo de datos de contenido.
7.  Suponiendo que el tipo de contenido interno es "data", inicialice la estructura de datos [**\_ CMSG CTRL DECRYPT \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) y llame a [**CryptMsgControl,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)pasando CMSG CTRL DECRYPT y la dirección de la \_ \_ estructura. El contenido se descifrará.
8.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)y pase CMSG CONTENT PARAM para obtener un puntero al blob de datos de contenido descodificado \_ \_ **(cadena BYTE).**
9.  Llame [**a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

El resultado de este procedimiento es que el mensaje se descodifica y descifra y se recupera un puntero al blob de datos de contenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programa C de ejemplo: codificación de un mensaje con sobres firmado](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
