---
description: Cifra un mensaje para proporcionar privacidad.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Función EncryptMessage (General) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6645d58b753503853dae7998982a32221d1f0d14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575401"
---
# <a name="encryptmessage-general-function"></a>Función EncryptMessage (General)

La **función EncryptMessage (General)** cifra un mensaje para proporcionar [*privacidad.*](../secgloss/p-gly.md) **EncryptMessage (General) permite** que una aplicación elija entre los algoritmos [*criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La **función EncryptMessage (General)** usa el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes que cifrar o descifrar, sino que proporcionan un hash de [*integridad*](../secgloss/h-gly.md) que se puede comprobar.

Cuando se usa el proveedor [*de compatibilidad de seguridad implícita*](../secgloss/s-gly.md) (SSP), esta función solo está disponible como mecanismo SASL.

Cuando se usa SChannel SSP, esta función [](../secgloss/s-gly.md) cifra los mensajes mediante una clave de sesión negociada con la parte remota que recibirá el mensaje. El algoritmo de cifrado viene determinado por el conjunto [ [*de cifrado*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en uso.

> [!Note]  
> Se puede llamar a **EncryptMessage (General)** y [**DecryptMessage (General)**](decryptmessage--general.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrado y el otro está descifrando. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

Para obtener información sobre el uso de esta función con un SSP específico, vea los temas siguientes.

| Tema                                                            | Descripción                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (digest)**](encryptmessage--digest.md)       | Cifra un mensaje para proporcionar privacidad mediante Digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Cifra un mensaje para proporcionar privacidad mediante Kerberos.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Cifra un mensaje para proporcionar privacidad mediante Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Cifra un mensaje para proporcionar privacidad mediante NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Cifra un mensaje para proporcionar privacidad mediante Schannel.  |

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

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero.

Este parámetro puede ser una de las marcas siguientes.


| Value | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Generar un encabezado o finalizador, pero no cifrar el mensaje.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br /> | 
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl><dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt></dl> | Enviar un mensaje de alerta de Schannel. En este caso, el <em>parámetro pMessage</em> debe contener un código de evento SSL/TLS estándar de dos bytes. Este valor solo es compatible con el SSP de Schannel.<br /> | 


*pMessage* \[ in, out\]

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Uno de ellos puede ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje que se va a cifrar. El mensaje se cifra en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa búferes con el atributo SECBUFFER \_ READONLY.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene de la función [**QueryContextAttributes (General) (SECPKG**](querycontextattributes--general.md) \_ ATTR \_ STREAM \_ SIZES).

Al usar el SSP de resumen, debe haber un segundo búfer de tipo SECBUFFER PADDING o SEC BUFFER DATA para contener \_ \_ información \_ [*de*](../secgloss/d-gly.md#_security_digital_signature_gly) firma. Para obtener el tamaño del búfer de salida, llame a la [**función QueryContextAttributes (General)**](querycontextattributes--general.md) y especifique SECPKG \_ ATTR \_ SIZES. La función devolverá una estructura [**SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) El tamaño del búfer de salida es la suma de los valores de los **miembros cbMaxSignature** **y cbBlockSize.**

Las aplicaciones que no usan SSL deben proporcionar [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SECBUFFER \_ PADDING.

*MessageSeqNo* \[ En\]

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe ser cero.

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero. El SSP de resumen administra la numeración de secuencia internamente.

Cuando se usa SChannel SSP, este parámetro debe establecerse en cero. Schannel SSP no usa números de secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BÚFER \_ E DE S DEMASIADO \_ \_ \_ PEQUEÑO**      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.                                                                                                          |
| **SEG \_ E CONTEXT EXPIRED (CONTEXTO E DE SEC \_ E \_ EXPIRADO)**        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error.                                        |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad.                                                                       |
| **S \_ E \_ MEMORIA \_ INSUFICIENTE**    | No hay suficiente memoria disponible para completar la acción solicitada.                                                                                                      |
| **IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.*                                                                                              |
| **TOKEN \_ NO VÁLIDO DE SEC E \_ \_**          | No se encontró ningún \_ búfer de tipo DE DATOS SECBUFFER.                                                                                                                                   |
| **SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**     | El contexto de seguridad [*no*](../secgloss/i-gly.md) admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md) |

## <a name="remarks"></a>Observaciones

La **función EncryptMessage (General)** cifra un mensaje basado en el mensaje y la clave [*de sesión*](../secgloss/s-gly.md) de un contexto de [*seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó [*el*](../secgloss/s-gly.md) contexto de seguridad para admitir la detección de secuencia y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia pasado desde la aplicación de transporte.

Cuando use el SSP de resumen, obtenga el tamaño del búfer de salida llamando a la función [**QueryContextAttributes (General)**](querycontextattributes--general.md) y especificando SECPKG \_ ATTR \_ SIZES. La función devolverá una estructura [**SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) El tamaño del búfer de salida es la suma de los valores de los **miembros cbMaxSignature** **y cbBlockSize.**

Cuando se usa con Schannel SSP, el *parámetro pMessage* debe contener una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con los búferes siguientes.

> [!Note]  
> Estos búferes deben proporcionarse en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| ENCABEZADO DE \_ SECUENCIA DE \_ SECBUFFER  | Utilizado de forma interna. No se requiere inicialización.                                                |
| DATOS DE \_ SECBUFFER            | Contiene el [*mensaje de texto no*](../secgloss/s-gly.md) cifrado que se va a cifrar. |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER | Utilizado de forma interna. No se requiere inicialización.                                                |
| SECBUFFER \_ EMPTY           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                              |

Cuando use SChannel SSP, determine el tamaño máximo de cada uno de los búferes llamando a la función [**QueryContextAttributes (General)**](querycontextattributes--general.md) y especificando el atributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Esta función devuelve una estructura [**SecPkgContext \_ StreamSizes cuyos**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) miembros contienen los tamaños máximos para los búferes de encabezado **(miembro cbHeader),** message **(miembro cbMaximumMessage)** y finalizador **(miembro cbTrailer).**

Para obtener un rendimiento óptimo, *las estructuras pMessage* se deben asignar desde la memoria contigua.

**Windows XP/2000:** Esta función también se conocía como **SealMessage.** Las aplicaciones ahora solo **deben usar EncryptMessage (General).**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio XP\]                                                            |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\]                                                   |
| Encabezado                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Consulte también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (General)**](decryptmessage--general.md)
- [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (General)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
