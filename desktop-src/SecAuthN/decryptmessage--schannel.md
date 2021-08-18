---
description: Descifra un mensaje mediante Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: Función DecryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: feec97f9e989270d812458cd61ff34132d118d192108c3f2372b192f2e383464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008483"
---
# <a name="decryptmessage-schannel-function"></a>Función DecryptMessage (Schannel)

La **función DecryptMessage (Schannel)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash de integridad.*](../secgloss/h-gly.md)


Esta función también se usa [](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) con el proveedor de compatibilidad de seguridad (SSP) de Schannel para señalar una solicitud de un remitente de mensajes para una renegociación (rehacer) de los atributos de conexión o para un cierre de la conexión.

> [!Note]  
> Se puede llamar a [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) y **DecryptMessage (Schannel)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) (SSPI) si se cifra un subproceso y el otro se descifra. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.


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


Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) se va a usar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Una de ellas puede ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en su lugar, sobrescribiendo el contenido original de su búfer.

Cuando se usa el SSP de Schannel con contextos que no están orientados a la conexión, en la entrada, la estructura debe contener cuatro [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Exactamente un búfer debe ser de tipo SECBUFFER \_ DATA y contener un mensaje cifrado, que se descifra en su lugar. Los búferes restantes se usan para la salida y deben ser de tipo SECBUFFER \_ EMPTY. En el caso de los contextos orientados a la conexión, se debe proporcionar un búfer de tipo SECBUFFER DATA, como se indica para contextos no orientados a \_ la conexión. Además, también se debe proporcionar un segundo búfer de tipo SECBUFFER TOKEN que contenga \_ un token de seguridad.

*MessageSeqNo* \[ En\]

Número de secuencia esperado por la aplicación de transporte, si lo hay. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe establecerse en cero.

Cuando se usa el SSP de Schannel, este parámetro debe establecerse en cero. Schannel SSP no usa números de secuencia.

*pfQOP* \[ out\]

Puntero a una variable de tipo **ULONG** que recibe marcas específicas del paquete que indican la calidad de protección.

Cuando se usa el SSP de Schannel, este parámetro no se usa y debe establecerse en **NULL.**

Este parámetro puede ser la marca siguiente.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>El mensaje no se ha cifrado, pero se ha generado un encabezado o finalizador.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se recibió en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**     | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.* Se usa con el SSP de Schannel.     |
| **TOKEN \_ NO VÁLIDO DE SEC E \_ \_**      | Los búferes son del tipo incorrecto o no se encontró ningún búfer de tipo SECBUFFER \_ DATA. Se usa con el SSP de Schannel.  |
| **SEG \_ E \_ MESSAGE \_ ALTERED**    | El mensaje se ha modificado. Se usa con el SSP de Schannel.                                                      |
| **S \_ E FUERA DE \_ \_ \_ SECUENCIA**   | El mensaje no se recibió en la secuencia correcta.                                                          |
| **SEG \_ I \_ CONTEXT \_ EXPIRED**    | El remitente del mensaje ha terminado de usar la conexión y ha iniciado un apagado. Para obtener información sobre cómo iniciar o reconocer un apagado, vea [Apagar una conexión Schannel.](shutting-down-an-schannel-connection.md) Se usa con el SSP de Schannel. |
| **SEC \_ I \_ RENEGOTIATE**         | La entidad remota requiere una nueva secuencia de protocolo de enlace o la aplicación acaba de iniciar un apagado. Vuelva al bucle de negociación y llame a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel),**](initializesecuritycontext--schannel.md)pase SECBUFFER_EXTRA devuelto desde DecryptMessage(). No se admite la renegociación para el modo kernel de Schannel. El autor de la llamada debe omitir este valor devuelto o apagar la conexión. Si se omite el valor, el cliente o el servidor podrían apagar la conexión como resultado. |


## <a name="remarks"></a>Comentarios

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Schannel)** y detectará que **DecryptMessage (Schannel)** se ha creado correctamente, pero los búferes de salida están vacíos. Este es un comportamiento normal y las aplicaciones deben ser capaces de abordarlo.

Cuando se usa Schannel SSP, la función [**DecryptMessage (General)**](decryptmessage--general.md) devuelve SEC I CONTEXT EXPIRED cuando el remitente del mensaje \_ ha cerrado la \_ \_ conexión. Para obtener información sobre cómo iniciar o reconocer un apagado, vea [Apagar una conexión Schannel.](shutting-down-an-schannel-connection.md)

Si usa TLS 1.0, es posible que tenga que llamar a esta función varias veces, ajustando el búfer de entrada en cada llamada, para descifrar un mensaje completo.


La **función DecryptMessage (Schannel)** devuelve SEC I RENEGOTIATE cuando el remitente del mensaje desea \_ \_ renegociar la conexión (contexto [*de seguridad*](../secgloss/s-gly.md)). Una aplicación controla una renegociación solicitada mediante una llamada a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (lado servidor) o [**InitializeSecurityContext (Schannel) (lado**](initializesecuritycontext--schannel.md) cliente) y pasa SECBUFFER_EXTRA devuelto desde DecryptMessage(). Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión. Para obtener más información, vea [Crear un contexto de seguridad de Schannel.](creating-an-schannel-security-context.md)


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Header                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
