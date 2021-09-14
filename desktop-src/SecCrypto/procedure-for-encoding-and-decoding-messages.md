---
description: Detalla el procedimiento para codificar un mensaje general.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Procedimiento para codificar y codificar mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170897"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Procedimiento para codificar y codificar mensajes

El procedimiento para codificar un mensaje general es el siguiente.

**Para codificar un mensaje**

1.  Inicialice las estructuras de datos adecuadas para el tipo de datos deseado.
2.  Llame [**a CryptMsgOpenToEncode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)pase los argumentos necesarios. Al llamar a **CryptMsgOpenToEncode**, si los datos que se van a proporcionar a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) ya se han codificado en mensajes, pase el identificador de objeto adecuado en *pszInnerContentObjID* (por ejemplo, "1.2.840.113549.1.7.2" para szOID \_ RSA \_ signedData). Si *pszInnerContentObjID* es [](../secgloss/i-gly.md) **NULL,** se supone que el tipo de contenido interno no se ha codificado previamente y se procesa correctamente.
3.  Llame [**a CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) tantas veces como sea necesario para completar el mensaje. En la última llamada, establezca el *parámetro fFinal* en **TRUE.** (Para obtener más información, **vea CryptMsgUpdate**).
4.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obtener un puntero a los parámetros deseados, como el contenido. Para codificar datos simples y generales, use CMSG \_ CONTENT \_ PARAM para *dwParamtype*.
5.  Cierre el mensaje mediante una [**llamada a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).

Este procedimiento genera un mensaje codificado de un tipo especificado en las llamadas de función.

El procedimiento para la decodificación de un mensaje general es el siguiente.

**Para descodificar un mensaje**

1.  Determine la longitud necesaria para que el búfer mantenga los datos codificados mediante [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).
2.  Llame [**a CryptMsgOpenToDecode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)pase los argumentos necesarios. Para mantener la compatibilidad Internet Explorer versión 3.0, se proporciona el parámetro *dwMsgType.* Los datos firmados creados Internet Explorer 3.0 no contienen información de encabezado. Por lo tanto, si este tipo de mensaje se extrae de las firmas de archivo, el tipo de mensaje debe pasarse a la función . Si se pasa cero al *parámetro dwMsgType,* la función leerá el tipo de mensaje del encabezado del mensaje. Si falta el encabezado, se producirá un error en la llamada a la función. Si se realiza correctamente, se devuelve un identificador para el mensaje abierto.
3.  Llame [**a CryptMsgUpdate una**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) vez. Esto hace que se tome las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Para un procesamiento adicional del mensaje, como descifrado adicional o comprobación de firma, llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)y pase la acción deseada *en dwCtrlType*.
5.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para obtener un puntero a los parámetros deseados, como el contenido. Para descodificar datos generales simples, use CMSG \_ CONTENT \_ PARAM para el *parámetro dwParamtype.*
6.  Llame [**a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

Para obtener un ejemplo que implementa estos pasos, vea [Ejemplo de programa C: Codificación](example-c-program-encoding-and-decoding-data.md)y codificación de datos . Para obtener procedimientos y un ejemplo que muestra el proceso de codificación, codificación y comprobación de la firma de un mensaje firmado, vea Programa C de [ejemplo: firma, codificación,](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)codificación y comprobación de un mensaje .

 

 
