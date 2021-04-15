---
description: Descifra un mensaje mediante el uso de Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: DecryptMessage (síntesis) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5363a5efc79d78c9c88e4a817c1c341e0e0f9c02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497693"
---
# <a name="decryptmessage-digest-function"></a>DecryptMessage (síntesis) (función)

La función **DecryptMessage (digest)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.

El [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) implícita (SSP) proporciona confidencialidad de cifrado y descifrado para los mensajes intercambiados entre el cliente y el servidor como un mecanismo SASL únicamente.

> [!Note]  
> Se puede llamar a [**EncryptMessage (digest)**](encryptmessage--digest.md) y **DecryptMessage (digest)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

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

*phContext* \[ de\]

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Al menos uno de estos datos debe ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.

Al usar el SSP de síntesis, en la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos debe ser de tipo SECBUFFER \_ Data o SECBUFFER \_ Stream y debe contener el mensaje cifrado.

*MessageSeqNo* \[ de\]

El número de secuencia esperado por la aplicación de transporte, si existe. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.

Al usar el SSP de síntesis, este parámetro debe establecerse en cero. El SSP de síntesis administra la numeración de secuencias internamente.

*pfQOP* \[ enuncia\]

Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.

Este parámetro puede ser una de las marcas siguientes.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>No se cifró el mensaje, pero se produjo un encabezado o un finalizador.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Al usar el SSP de síntesis, use esta marca cuando el [*contexto de seguridad*](../secgloss/s-gly.md) esté establecido para comprobar solo la [*firma*](../secgloss/s-gly.md) . Para obtener más información, consulte [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **búfer de s \_ E s \_ \_ demasiado \_ pequeño**      | El búfer de mensajes es demasiado pequeño. Se usa con el SSP de síntesis.                                                                                                                   |
| **s \_ E \_ \_ sistema criptográfico \_ no válido** | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) . Se usa con el SSP de síntesis.                                                                                       |
| **s \_ E \_ mensaje incompleto \_**     | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y llamar de nuevo a [**DecryptMessage (síntesis)**](decryptmessage--digest.md) . |
| **s \_ E \_ identificador no válido \_**         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* . Se usa con el SSP de síntesis.                                                                     |
| **s \_ E \_ mensaje \_ modificado**        | El mensaje se ha modificado. Se usa con el SSP de síntesis.                                                                                                                      |
| **s \_ E \_ fuera \_ de \_ secuencia**       | No se recibió el mensaje en la secuencia correcta.                                                                                                                        |
| **s \_ E \_ QOP \_ no \_ admitidos**     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md). Se usa con el SSP de síntesis.                           |

## <a name="remarks"></a>Observaciones

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (digest)** y detectará que **DecryptMessage (digest)** se ejecutó correctamente, pero los búferes de salida están vacíos. Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora deben usar **DecryptMessage (digest)** solamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\]          |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\] |
| Encabezado                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | SECUR32. lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Resumen)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
