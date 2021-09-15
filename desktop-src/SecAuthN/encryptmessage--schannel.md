---
description: Cifra un mensaje para proporcionar privacidad mediante Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Función EncryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3075b2fe7e5b4167a5a8527a16009282b2fca1b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575393"
---
# <a name="encryptmessage-schannel-function"></a>Función EncryptMessage (Schannel)

La **función EncryptMessage (Schannel)** cifra un mensaje para proporcionar [*privacidad.*](../secgloss/p-gly.md) **EncryptMessage (Schannel) permite** que una aplicación elija entre los algoritmos [*criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La **función EncryptMessage (Schannel)** usa el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes que cifrar o descifrar, sino que proporcionan un hash de [*integridad*](../secgloss/h-gly.md) que se puede comprobar.

Cuando se usa Schannel SSP, esta función [](../secgloss/s-gly.md) cifra los mensajes mediante una clave de sesión negociada con la parte remota que recibirá el mensaje. El algoritmo de cifrado viene determinado por el conjunto [ [*de cifrado*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en uso.

> [!Note]  
> Se puede llamar a **EncryptMessage (Schannel)** y [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si se cifra un subproceso y el otro se descifra. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

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

*phContext* \[ En\]

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para cifrar el mensaje.

*fQOP* \[ En\]

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Este parámetro puede ser la marca siguiente.

| Value                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ WRAP \_ OOB \_ DATA**</dt> </dl> | Enviar un mensaje de alerta de Schannel. En este caso, el *parámetro pMessage* debe contener un código de evento SSL/TLS estándar de dos bytes. Este valor solo es compatible con el SSP de Schannel.<br/> Por ejemplo, a partir de Windows Vista, el mensaje "server hello" enviado por el servidor durante el protocolo de autenticación de nuevo debe cifrarse como una alerta TLS.<br/> |

*pMessage* \[ in, out\]

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno de ellos puede ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje que se va a cifrar. El mensaje se cifra en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa búferes con el atributo SECBUFFER \_ READONLY.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene de la función [**QueryContextAttributes (Schannel) (SECPKG**](querycontextattributes--schannel.md) \_ ATTR \_ STREAM \_ SIZES).

*MessageSeqNo* \[ En\]

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe ser cero.

Cuando se usa SChannel SSP, este parámetro debe establecerse en cero. Schannel SSP no usa números de secuencia.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                                                                                                    | Descripción                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BÚFER \_ E DE S DEMASIADO \_ \_ \_ PEQUEÑO**</dt> </dl>      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.<br/>                                                                               |
| <dl> <dt>**SEG \_ E CONTEXT EXPIRED (CONTEXTO E DE SEC \_ E \_ EXPIRADO)**</dt> </dl>        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error.<br/>             |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad.<br/>                       |
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>    | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                           |
| <dl> <dt>**IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.*<br/>                                                                   |
| <dl> <dt>**TOKEN \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>          | No se encontró ningún \_ búfer de tipo DE DATOS SECBUFFER.<br/>                                                                                                        |
| <dl> <dt>**SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**</dt> </dl>     | El contexto de seguridad [*no*](../secgloss/i-gly.md) admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md)<br/> |

## <a name="remarks"></a>Observaciones

La **función EncryptMessage (Schannel)** cifra un mensaje basado en el mensaje y la clave [*de sesión*](../secgloss/s-gly.md) desde un contexto de [*seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó [*el*](../secgloss/s-gly.md) contexto de seguridad para admitir la detección de secuencia y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

Cuando se usa con Schannel SSP, el *parámetro pMessage* debe contener una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con los búferes siguientes.

> [!Note]  
> Estos búferes deben proporcionarse en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| ENCABEZADO DE \_ SECUENCIA DE \_ SECBUFFER  | Utilizado de forma interna. No se requiere inicialización.                                                                        |
| DATOS DE \_ SECBUFFER            | Contiene el [*mensaje de texto no*](../secgloss/s-gly.md) cifrado que se va a cifrar. |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER | Utilizado de forma interna. No se requiere inicialización.                                                                        |
| SECBUFFER \_ EMPTY           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                                                      |

Cuando use Schannel SSP, determine el tamaño máximo de cada uno de los búferes llamando a la función [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) y especificando el atributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Esta función devuelve una estructura [**SecPkgContext \_ StreamSizes cuyos**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) miembros contienen los tamaños máximos para los búferes de encabezado **(miembro cbHeader),** message **(miembro cbMaximumMessage)** y finalizador **(miembro cbTrailer).**

Para obtener un rendimiento óptimo, las *estructuras pMessage* se deben asignar desde la memoria contigua.

**Windows XP/2000:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora solo **deben usar EncryptMessage (Schannel).**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Encabezado                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Consulte también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
