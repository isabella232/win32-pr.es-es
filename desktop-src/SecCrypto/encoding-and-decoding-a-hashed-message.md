---
description: Muestra las tareas necesarias para codificar un mensaje con hash.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codificación y codificación de un mensaje con hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bed6ffae240d9139de471f16dcaaf2ed3e29d5bc92c8d7507b981c2af67541c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766751"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codificación y codificación de un mensaje con hash

Los datos con hash constan de contenido de cualquier tipo y [*un hash*](../secgloss/h-gly.md) del contenido. Se puede usar cuando solo es necesario confirmar que el contenido del mensaje no se ha modificado desde que se creó el hash.

Al crear un mensaje con hash, puede haber varios algoritmos hash y varios hashes. En la ilustración siguiente se muestran las tareas necesarias para codificar un mensaje con hash. El procedimiento se describe en el texto que sigue a la ilustración.

![crear un mensaje con hash](images/hashmsg.png)

**Para crear un mensaje con hash**

1.  Obtenga un puntero a los datos a los que se va a hash.
2.  Seleccione el algoritmo hash que se va a usar.
3.  Coloque los datos a través de una función hash mediante el algoritmo hash.
4.  Incluya los datos originales a los que se va a aplicar un algoritmo hash, los algoritmos hash y los hashes en el mensaje codificado.

Para usar funciones de mensaje de bajo nivel para realizar las tareas que se han descrito, use el procedimiento siguiente.

**Para crear un algoritmo hash y codificar un mensaje mediante funciones de mensaje de bajo nivel**

1.  Cree o recupere el contenido que se va a hash.
2.  Obtener un proveedor de servicios criptográficos.
3.  Inicialice la [**estructura \_ CMSG HASHED \_ ENCODE \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info)
4.  Llame [**a CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del blob del mensaje codificado. Asigne memoria para él.
5.  Llame a [**CryptMsgOpenToEncode,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)pasando CMSG HASHED para el parámetro dwMsgType y un puntero a \_  [**\_ CMSG HASHED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) para el parámetro *pvMsgEncodeInfo.* Como resultado de esta llamada, se obtiene un identificador para el mensaje abierto.
6.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 5 y un puntero a los datos que se deben codificar y codificar. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
7.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 5 y los tipos de parámetro adecuados para acceder a los datos codificados deseados. Por ejemplo, pase CMSG CONTENT PARAM para \_ obtener un puntero a todo el mensaje \_ [*PKCS \# 7.*](../secgloss/p-gly.md)

    Si el resultado de esta codificación [](../secgloss/i-gly.md) se va a usar como datos internos para otro mensaje codificado, como un mensaje con sobres, se debe pasar CMSG \_ BARE CONTENT \_ \_ PARAM. Para obtener un ejemplo en el que se muestra esto, vea [Código alternativo para codificar un mensaje con sobres](alternate-code-for-encoding-an-enveloped-message.md).

8.  Cierre el mensaje mediante una [**llamada a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado que contiene los datos originales, los algoritmos hash y [*el hash*](../secgloss/h-gly.md) de los datos. En el paso 7 se obtiene un puntero al [*mensaje codificado BLOB.*](../secgloss/b-gly.md)

Los dos procedimientos siguientes descodifican y, a continuación, comprueban los datos con hash.

**Para descodificar datos con hash**

1.  Obtenga un puntero al BLOB codificado.
2.  Llame [**a CryptMsgOpenToDecode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)pase los argumentos necesarios.
3.  Llame [**a CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se descodificarán. Esto hace que se tome las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 2 y los tipos de parámetro adecuados para acceder a los datos descodificados deseados. Por ejemplo, pase CONTENT PARAM de CMSG \_ para obtener un puntero al contenido \_ descodificado.

**Para comprobar el hash**

1.  Llame [**a CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)y pase CMSG \_ CTRL VERIFY HASH para comprobar los \_ \_ hashes.
2.  Llame [**a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

Para obtener un programa de ejemplo, vea [Programa de C de ejemplo: Codificación y decodización de un mensaje con hash](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
