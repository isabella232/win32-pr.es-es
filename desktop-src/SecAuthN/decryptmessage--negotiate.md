---
description: Descifra un mensaje mediante Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Función DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5587b9faef4cbb44cfe8d30841de31ef1147e7ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468152"
---
# <a name="decryptmessage-negotiate-function"></a>Función DecryptMessage (Negotiate)

La **función DecryptMessage (Negotiate)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash de integridad.*](../secgloss/h-gly.md)

> [!Note]  
> Se puede llamar a [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) y **DecryptMessage (Negotiate)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si se cifra un subproceso y el otro se descifra. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

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

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Al menos uno de ellos debe ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en su lugar, sobrescribiendo el contenido original de su búfer.

*MessageSeqNo* \[ En\]

Número de secuencia esperado por la aplicación de transporte, si lo hay. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe establecerse en cero.

*pfQOP* \[ out\]

Puntero a una variable de tipo **ULONG** que recibe marcas específicas del paquete que indican la calidad de protección.

Este parámetro puede ser la marca siguiente.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | El mensaje no se ha cifrado, pero se ha generado un encabezado o finalizador.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br /> | 


## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se recibió en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MENSAJE \_ INCOMPLETO DE SEC E \_ \_** | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y volver a llamar [**a DecryptMessage (Negotiate).**](decryptmessage--negotiate.md) |
| **SEC \_ E \_ OUT \_ OF \_ SEQUENCE**   | El mensaje no se recibió en la secuencia correcta.                                                                                                                              |

## <a name="remarks"></a>Comentarios

A veces, una aplicación leerá los datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Negotiate)** y detectará que **DecryptMessage (Negotiate)** se ha hecho correctamente, pero los búferes de salida están vacíos. Este es un comportamiento normal y las aplicaciones deben ser capaces de abordarlo.

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora solo **deben usar DecryptMessage (Negotiate).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Encabezado                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Consulte también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
