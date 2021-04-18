---
description: Descifra un mensaje mediante Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: DecryptMessage (Negotiate) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720386"
---
# <a name="decryptmessage-negotiate-function"></a>DecryptMessage (Negotiate) (función)

La función **DecryptMessage (Negotiate)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.

> [!Note]  
> Se puede llamar a [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) y **DecryptMessage (Negotiate)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

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

*phContext* \[ de\]

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Al menos uno de estos datos debe ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.

*MessageSeqNo* \[ de\]

El número de secuencia esperado por la aplicación de transporte, si existe. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.

*pfQOP* \[ enuncia\]

Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.

Este parámetro puede ser la marca siguiente.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>No se cifró el mensaje, pero se produjo un encabezado o un finalizador.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ mensaje incompleto \_** | Los datos del búfer de entrada están incompletos. La aplicación necesita leer más datos del servidor y llamar a [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) de nuevo. |
| **s \_ E \_ fuera \_ de \_ secuencia**   | No se recibió el mensaje en la secuencia correcta.                                                                                                                              |

## <a name="remarks"></a>Observaciones

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Negotiate)** y detectará que **DecryptMessage (Negotiate)** se ejecutó correctamente, pero los búferes de salida están vacíos. Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora deben usar **DecryptMessage (Negotiate)** solamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\]          |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\] |
| Encabezado                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | SECUR32. lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
