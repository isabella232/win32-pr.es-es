---
description: Descifra un mensaje mediante Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: Función DecryptMessage (Digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f87828263766643a10cf5400e38cabe9d3096403
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480871"
---
# <a name="decryptmessage-digest-function"></a>Función DecryptMessage (Digest)

La **función DecryptMessage (Digest)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash de integridad.*](../secgloss/h-gly.md)

El proveedor de [*compatibilidad de seguridad implícita*](../secgloss/s-gly.md) (SSP) proporciona confidencialidad de cifrado y descifrado para los mensajes intercambiados entre el cliente y el servidor como un mecanismo SASL únicamente.

> [!Note]  
> Se puede llamar a [**EncryptMessage (Digest)**](encryptmessage--digest.md) y **DecryptMessage (Digest)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si se cifra un subproceso y el otro se descifra. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a>Parámetros

*phContext* \[ En\]

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Al menos uno de ellos debe ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en su lugar, sobrescribiendo el contenido original de su búfer.

Cuando se usa el SSP de resumen, en la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Una de ellas debe ser de tipo SECBUFFER \_ DATA o SECBUFFER \_ STREAM y debe contener el mensaje cifrado.

*MessageSeqNo* \[ En\]

Número de secuencia esperado por la aplicación de transporte, si lo hay. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe establecerse en cero.

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero. El SSP de resumen administra la numeración de secuencia internamente.

*pfQOP* \[ out\]

Puntero a una variable de tipo **ULONG** que recibe marcas específicas del paquete que indican la calidad de protección.

Este parámetro puede ser una de las marcas siguientes.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | El mensaje no se ha cifrado, pero se ha generado un encabezado o finalizador.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Cuando use el SSP de resumen, use esta marca cuando el contexto [*de*](../secgloss/s-gly.md) seguridad esté establecido para comprobar solo [*la firma.*](../secgloss/s-gly.md) Para obtener más información, vea [Calidad de protección.](quality-of-protection.md)<br /> | 


## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se recibió en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BÚFER \_ E DE S DEMASIADO \_ \_ \_ PEQUEÑO**      | El búfer de mensajes es demasiado pequeño. Se usa con el SSP de resumen.                                                                                                                   |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad. Se usa con el SSP de resumen.                                                                                       |
| **MENSAJE \_ INCOMPLETO DE SEC E \_ \_**     | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y volver a llamar [**a DecryptMessage (Digest).**](decryptmessage--digest.md) |
| **IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.* Se usa con el SSP de resumen.                                                                     |
| **SEG \_ E \_ MESSAGE \_ ALTERED**        | El mensaje se ha modificado. Se usa con el SSP de resumen.                                                                                                                      |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**       | El mensaje no se recibió en la secuencia correcta.                                                                                                                        |
| **SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**     | El contexto de seguridad [*no*](../secgloss/i-gly.md) admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md) Se usa con el SSP de resumen.                           |

## <a name="remarks"></a>Comentarios

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Digest)** y detectará que **DecryptMessage (Digest)** se ha creado correctamente, pero los búferes de salida están vacíos. Este es un comportamiento normal y las aplicaciones deben ser capaces de abordarlo.

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora solo **deben usar DecryptMessage (Digest).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Encabezado                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Consulte también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (digest)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
