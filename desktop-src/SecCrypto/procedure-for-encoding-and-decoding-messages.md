---
description: Detalla el procedimiento para codificar un mensaje general.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Procedimiento para codificar y descodificar mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687362"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Procedimiento para codificar y descodificar mensajes

El procedimiento para codificar un mensaje general es el siguiente.

**Para codificar un mensaje**

1.  Inicializa las estructuras de datos adecuadas para el tipo de datos deseado.
2.  Llame a [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), pasando los argumentos necesarios. Al llamar a **CryptMsgOpenToEncode**, si los datos que se van a proporcionar a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) ya se han codificado por mensaje, pase el identificador de objeto adecuado en *pszInnerContentObjID* (por ejemplo, "1.2.840.113549.1.7.2" para szOID \_ RSA \_ signedData). Si *pszInnerContentObjID* es **null**, se supone que el tipo de [*contenido interno*](../secgloss/i-gly.md) no se ha codificado previamente y se procesa correctamente.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) tantas veces como sea necesario para completar el mensaje. En la última llamada, establezca el parámetro *fFinal* en **true**. (Para obtener más información, consulte **CryptMsgUpdate**).
4.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obtener un puntero a los parámetros deseados, como el contenido. Para codificar datos simples y generales, use \_ \_ el parámetro de contenido CMSG para el *dwParamtype*.
5.  Cierre el mensaje mediante una llamada a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Este procedimiento da como resultado un mensaje codificado de un tipo especificado en las llamadas de función.

El procedimiento para descodificar un mensaje general es el siguiente.

**Para descodificar un mensaje**

1.  Determine la longitud necesaria para que el búfer contenga los datos codificados mediante [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).
2.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios. Para mantener la compatibilidad con Internet Explorer versión 3,0, se proporciona el parámetro *dwMsgType* . Los datos firmados creados en Internet Explorer 3,0 no contienen información de encabezado. Por lo tanto, si este mensaje se extrae de las firmas de archivo, el tipo de mensaje se debe pasar a la función. Si se pasa cero al parámetro *dwMsgType* , la función leerá el tipo de mensaje del encabezado del mensaje. Si falta el encabezado, se producirá un error en la llamada de función. Si se realiza correctamente, se devuelve un identificador al mensaje abierto.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez. Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Para el procesamiento adicional del mensaje, como el descifrado adicional o la comprobación de la firma, llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando la acción deseada en *dwCtrlType*.
5.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obtener un puntero a los parámetros deseados, como el contenido. Para descodificar datos generales simples, use \_ \_ el parámetro de contenido CMSG para el parámetro *dwParamtype* .
6.  Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

Para obtener un ejemplo en el que se implementan estos pasos, vea [programa C de ejemplo: codificar y descodificar datos](example-c-program-encoding-and-decoding-data.md). Para obtener información sobre los procedimientos y un ejemplo en el que se muestra el proceso de codificación, descodificación y comprobación de la firma de un mensaje firmado, vea el [ejemplo de programa C: firma, codificación, descodificación y comprobación de un mensaje](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
