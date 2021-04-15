---
description: Cifra un mensaje para ofrecer privacidad mediante Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: EncryptMessage (Schannel) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3075b2fe7e5b4167a5a8527a16009282b2fca1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720694"
---
# <a name="encryptmessage-schannel-function"></a>EncryptMessage (Schannel) (función)

La función **EncryptMessage (Schannel)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md). **EncryptMessage (Schannel)** permite que una aplicación Elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La función **EncryptMessage (Schannel)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.

Cuando se usa Schannel SSP, esta función cifra los mensajes mediante una [*clave de sesión*](../secgloss/s-gly.md) negociada con la parte remota que recibirá el mensaje. El algoritmo de cifrado viene determinado por el conjunto de [ [*cifrado*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en uso.

> [!Note]  
> Se puede llamar a **EncryptMessage (Schannel)** y [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a>Parámetros

*phContext* \[ de\]

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.

*fQOP* \[ de\]

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Este parámetro puede ser la marca siguiente.

| Value                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ encapsular \_ \_ datos OOB**</dt> </dl> | Envíe un mensaje de alerta de Schannel. En este caso, el parámetro *pMessage* debe contener un código de evento SSL/TLS estándar de dos bytes. Este valor solo es compatible con el SSP de Schannel.<br/> Por ejemplo, a partir de Windows Vista, el mensaje "Hello Server" enviado por el servidor durante el protocolo de reautenticación se debe cifrar como una alerta de TLS.<br/> |

*pMessage* \[ in, out\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos puede ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje que se va a cifrar. El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) ( \_ ATTR \_ Stream \_ sizes).

*MessageSeqNo* \[ de\]

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.

Cuando se usa Schannel SSP, este parámetro debe establecerse en cero. Schannel SSP no utiliza números de secuencia.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                                                                                                    | Descripción                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**búfer de s \_ E s \_ \_ demasiado \_ pequeño**</dt> </dl>      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ contexto \_ expirado**</dt> </dl>        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error.<br/>             |
| <dl> <dt>**s \_ E \_ \_ sistema criptográfico \_ no válido**</dt> </dl> | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .<br/>                       |
| <dl> <dt>**s \_ E \_ memoria insuficiente \_**</dt> </dl>    | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                           |
| <dl> <dt>**s \_ E \_ identificador no válido \_**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .<br/>                                                                   |
| <dl> <dt>**s \_ E \_ token no válido \_**</dt> </dl>          | No \_ se encontró ningún búfer de tipo de datos SECBUFFER.<br/>                                                                                                        |
| <dl> <dt>**s \_ E \_ QOP \_ no \_ admitidos**</dt> </dl>     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md).<br/> |

## <a name="remarks"></a>Observaciones

La función **EncryptMessage (Schannel)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

Cuando se usa con el SSP de Schannel, el parámetro *pMessage* debe contener una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con los siguientes búferes.

> [!Note]  
> Estos búferes se deben proporcionar en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ encabezado de secuencia \_  | Utilizado de forma interna. No se requiere inicialización.                                                                        |
| datos de SECBUFFER \_            | Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar. |
| \_finalizador de flujo SECBUFFER \_ | Utilizado de forma interna. No se requiere inicialización.                                                                        |
| SECBUFFER \_ vacío           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                                                      |

Al usar el SSP de Schannel, determine el tamaño máximo de cada uno de los búferes mediante una llamada a la función [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) y especificando el \_ atributo SECPKG ATTR \_ Stream \_ sizes. Esta función devuelve una [**estructura SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cuyos miembros contienen los tamaños máximos para los búferes de encabezado (miembro **cbHeader** ), mensaje (miembro **cbMaximumMessage** ) y finalizador (miembro **cbTrailer** ).

Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.

**Windows XP/2000:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora deben usar **EncryptMessage (Schannel)** solamente.

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
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
