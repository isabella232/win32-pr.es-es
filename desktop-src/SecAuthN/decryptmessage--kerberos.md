---
description: Descifra un mensaje mediante Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Función DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 62add8d4b33f356aeae5bbbf8fa16b19a0b5e419e0ab6c0a6847a3ed087ce726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008543"
---
# <a name="decryptmessage-kerberos-function"></a>Función DecryptMessage (Kerberos)

La **función DecryptMessage (Kerberos)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash de integridad.*](../secgloss/h-gly.md)

> [!Note]  
> Se puede llamar a [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) y **DecryptMessage (Kerberos)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro se está descifrando. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a>Parámetros

*phContext* \[ En\]

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SECBUFFER \_ DATA. El búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en su lugar, sobrescribiendo el contenido original de su búfer.

*MessageSeqNo* \[ En\]

Número de secuencia esperado por la aplicación de transporte, si lo hay. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe establecerse en cero.

*pfQOP* \[ out\]

Puntero a una variable de tipo **ULONG** que recibe marcas específicas del paquete que indican la calidad de protección.

Este parámetro puede ser la marca siguiente.

| Value                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | No se ha cifrado el mensaje, pero se ha producido un encabezado o finalizador. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se recibió en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ E \_ MENSAJE \_ INCOMPLETO** | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y volver a llamar [**a DecryptMessage (Kerberos).**](decryptmessage--kerberos.md) |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | El mensaje no se recibió en la secuencia correcta.                                                                                                                            |

## <a name="remarks"></a>Comentarios

A veces, una aplicación leerá los datos de la entidad remota, intentará descifrarlo mediante **DecryptMessage (Kerberos)** y detectará que **DecryptMessage (Kerberos)** se ha hecho correctamente, pero los búferes de salida están vacíos. Este es un comportamiento normal y las aplicaciones deben ser capaces de tratar con él.

Para obtener información sobre cómo interoperar con GSSAPI, vea [Interoperabilidad de SSPI/Kerberos con GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora solo **deben usar DecryptMessage (Kerberos).**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio XP\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Header                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
