---
description: Describe las tareas necesarias para codificar un mensaje con hash.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codificar y descodificar un mensaje con hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668233"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codificar y descodificar un mensaje con hash

Los datos con hash se componen de contenido de cualquier tipo y un [*hash*](../secgloss/h-gly.md) del contenido. Se puede usar cuando solo es necesario confirmar que el contenido del mensaje no se ha modificado desde que se creó el hash.

Al crear un mensaje con hash, puede haber varios algoritmos hash y varios valores hash. En la ilustración siguiente se muestran las tareas necesarias para codificar un mensaje con hash. El procedimiento se describe en el texto que sigue a la ilustración.

![crear un mensaje con hash](images/hashmsg.png)

**Para crear un mensaje con hash**

1.  Obtiene un puntero a los datos a los que se va a aplicar un algoritmo hash.
2.  Seleccione el algoritmo hash que se va a usar.
3.  Coloque los datos a través de una función hash mediante el algoritmo hash.
4.  Incluya los datos originales a los que se va a aplicar un algoritmo hash, los algoritmos hash y los valores hash del mensaje codificado.

Para usar las funciones de mensaje de bajo nivel para realizar las tareas que se describen a continuación, utilice el procedimiento siguiente.

**Para aplicar un algoritmo hash y codificar un mensaje mediante funciones de mensaje de bajo nivel**

1.  Cree o recupere el contenido al que se va a aplicar un algoritmo hash.
2.  Obtener un proveedor de servicios criptográficos.
3.  Inicializa la estructura de [**\_ \_ \_ información de codificación hash de CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) .
4.  Llame a [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) para obtener el tamaño del BLOB del mensaje codificado. Asigne memoria.
5.  Llame a [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), pasando CMSG \_ hash para el parámetro *dwMsgType* y un puntero a la [**\_ \_ \_ información de codificación hash CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) para el parámetro *pvMsgEncodeInfo* . Como resultado de esta llamada, obtendrá un identificador para el mensaje abierto.
6.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), pasando el identificador recuperado en el paso 5 y un puntero a los datos a los que se va a aplicar un algoritmo hash y codificado. Se puede llamar a esta función tantas veces como sea necesario para completar el proceso de codificación.
7.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 5 y los tipos de parámetro adecuados para tener acceso a los datos codificados deseados. Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al mensaje [*PKCS \# 7*](../secgloss/p-gly.md) completo.

    Si el resultado de esta codificación se va a usar como [*datos internos*](../secgloss/i-gly.md) de otro mensaje codificado, como un mensaje con doble cifrado, \_ \_ \_ se debe pasar el parámetro CMSG de contenido sin sistema operativo. Para ver un ejemplo que muestra esto, consulte el [código alternativo para codificar un mensaje con doble cifrado](alternate-code-for-encoding-an-enveloped-message.md).

8.  Cierre el mensaje mediante una llamada a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

El resultado de este procedimiento es un mensaje codificado que contiene los datos originales, los algoritmos hash y el [*hash*](../secgloss/h-gly.md) de esos datos. En el paso 7 se obtiene un puntero al [*BLOB*](../secgloss/b-gly.md) del mensaje codificado.

Los dos procedimientos siguientes descodifican y comprueban los datos con hash.

**Para descodificar los datos con hash**

1.  Obtiene un puntero al objeto binario codificado.
2.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se van a descodificar. Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 2 y los tipos de parámetro adecuados para tener acceso a los datos descodificados deseados. Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al contenido descodificado.

**Para comprobar el hash**

1.  Llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando CMSG \_ Ctrl \_ Verify \_ hash para comprobar los valores hash.
2.  Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

Para obtener un programa de ejemplo, vea [ejemplo de programa C: codificar y descodificar un mensaje con hash](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
