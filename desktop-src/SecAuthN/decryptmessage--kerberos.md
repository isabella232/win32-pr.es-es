---
description: Descifra un mensaje mediante Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Función DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154772"
---
# <a name="decryptmessage-kerberos-function"></a>Función DecryptMessage (Kerberos)

La función **DecryptMessage (Kerberos)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.

> [!Note]  
> Se puede llamar a [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) y **DecryptMessage (Kerberos)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

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

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data. El búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.

*MessageSeqNo* \[ de\]

El número de secuencia esperado por la aplicación de transporte, si existe. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.

*pfQOP* \[ enuncia\]

Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.

Este parámetro puede ser la marca siguiente.

| Value                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | no se cifró el mensaje, pero se produjo un encabezado o finalizador. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ mensaje incompleto \_** | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y llamar de nuevo a [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) . |
| **s \_ E \_ fuera \_ de \_ secuencia**   | No se recibió el mensaje en la secuencia correcta.                                                                                                                            |

## <a name="remarks"></a>Observaciones

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Kerberos)** y detectará que **DecryptMessage (Kerberos)** se ejecutó correctamente, pero los búferes de salida están vacíos. Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.

Para obtener información acerca de cómo interoperar con GSSAPI, consulte [interoperabilidad de SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

**Windows XP:** Esta función también se conocía como **UnsealMessage**. Las aplicaciones ahora deben usar **DecryptMessage (Kerberos)** solamente.

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
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
