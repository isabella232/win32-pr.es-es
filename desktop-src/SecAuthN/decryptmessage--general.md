---
description: Descifra un mensaje.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: Función DecryptMessage (General) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9dfbde6c0b4a8c46920428af3d7f700268f11690
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476921"
---
# <a name="decryptmessage-general-function"></a>Función DecryptMessage (General)

La **función DecryptMessage (General)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash de integridad.*](../secgloss/h-gly.md)

El proveedor de [*compatibilidad de seguridad implícita*](../secgloss/s-gly.md) (SSP) proporciona confidencialidad de cifrado y descifrado para los mensajes intercambiados entre el cliente y el servidor como un mecanismo SASL únicamente.

Esta función también se usa con el SSP de Schannel para señalar una solicitud de un remitente del mensaje para una renegociación (rehacer) de los atributos de conexión o para un cierre de la conexión.

> [!Note]  
> Se puede llamar a [**EncryptMessage (General)**](encryptmessage--general.md) y **DecryptMessage (General)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrado y el otro está descifrando. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

 

Para obtener información sobre el uso de esta función con un SSP específico, vea los temas siguientes.



| Tema                                                            | Descripción                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (Digest)**](decryptmessage--digest.md)       | Descifra un mensaje mediante Digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Descifra un mensaje mediante Kerberos.  |
| [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) | Descifra un mensaje mediante Negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Descifra un mensaje mediante NTLM.      |
| [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)   | Descifra un mensaje mediante Schannel.  |



 

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

<dl> <dt>

*phContext* \[ En\]
</dt> <dd>

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para descifrar el mensaje.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Una de ellas puede ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en su lugar, sobrescribiendo el contenido original de su búfer.

Cuando se usa el SSP de resumen, en la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Una de ellas debe ser de tipo SECBUFFER \_ DATA o SECBUFFER \_ STREAM y debe contener el mensaje cifrado.

Cuando se usa el SSP de Schannel con contextos que no están orientados a la conexión, en la entrada, la estructura debe contener cuatro [**estructuras SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Exactamente un búfer debe ser de tipo SECBUFFER \_ DATA y contener un mensaje cifrado, que se descifra en su lugar. Los búferes restantes se usan para la salida y deben ser de tipo SECBUFFER \_ EMPTY. En el caso de los contextos orientados a la conexión, se debe proporcionar un búfer de tipo SECBUFFER DATA, como se indica para contextos no orientados a \_ la conexión. Además, también se debe proporcionar un segundo búfer de tipo SECBUFFER TOKEN que contenga \_ un token de seguridad.

</dd> <dt>

*MessageSeqNo* \[ En\]
</dt> <dd>

Número de secuencia esperado por la aplicación de transporte, si lo hay. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe establecerse en cero.

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero. El SSP de resumen administra la numeración de secuencia internamente.

Cuando se usa el SSP de Schannel, este parámetro debe establecerse en cero. Schannel SSP no usa números de secuencia.

</dd> <dt>

*pfQOP* \[ out\]
</dt> <dd>

Puntero a una variable de tipo **ULONG** que recibe marcas específicas del paquete que indican la calidad de protección.

Cuando se usa el SSP de Schannel, este parámetro no se usa y debe establecerse en **NULL.**

Este parámetro puede ser una de las marcas siguientes.




| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | El mensaje no se ha cifrado, pero se ha generado un encabezado o finalizador.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Cuando use el SSP de resumen, use esta marca cuando el contexto [*de*](../secgloss/s-gly.md) seguridad esté establecido para comprobar solo [*la firma.*](../secgloss/s-gly.md) Para obtener más información, vea [Calidad de protección.](quality-of-protection.md)<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se recibió en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BÚFER \_ E DE S DEMASIADO \_ \_ \_ PEQUEÑO**</dt> </dl>      | El búfer de mensajes es demasiado pequeño. Se usa con el SSP de resumen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad. Se usa con el SSP de resumen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**MENSAJE \_ INCOMPLETO DE SEC E \_ \_**</dt> </dl>     | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y volver a llamar [**a DecryptMessage (General).**](decryptmessage--general.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.* Se usa con los SSP digest y Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**TOKEN \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>          | Los búferes son del tipo incorrecto o no se encontró ningún búfer de tipo SECBUFFER \_ DATA. Se usa con el SSP de Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEG \_ E \_ MESSAGE \_ ALTERED**</dt> </dl>        | El mensaje se ha modificado. Se usa con los SSP digest y Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ OUT \_ OF \_ SEQUENCE**</dt> </dl>       | El mensaje no se recibió en la secuencia correcta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**</dt> </dl>     | El contexto de seguridad [*no*](../secgloss/i-gly.md) admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md) Se usa con el SSP de resumen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEG \_ I \_ CONTEXT \_ EXPIRED**</dt> </dl>        | El remitente del mensaje ha terminado de usar la conexión y ha iniciado un apagado. Para obtener información sobre cómo iniciar o reconocer un apagado, vea [Apagar una conexión Schannel.](shutting-down-an-schannel-connection.md) Se usa con el SSP de Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEG \_ I \_ RENEGOTIATE**</dt> </dl>             | La entidad remota requiere una nueva secuencia de protocolo de enlace o la aplicación acaba de iniciar un apagado. Vuelva al bucle de negociación y llame a [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) o [**InitializeSecurityContext (general),**](initializesecuritycontext--general.md)pasando búferes de entrada vacíos. <br/> Si la función devuelve un búfer de tipo **SEC \_ BUFFER \_ EXTRA,** debe pasarse a la [**función AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) como búfer de entrada.<br/> Se usa con el SSP de Schannel.<br/> No se admite la renegociación para el modo kernel de Schannel. El autor de la llamada debe omitir este valor devuelto o apagar la conexión. Si se omite el valor, el cliente o el servidor podrían apagar la conexión como resultado.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando se usa Schannel SSP, la función **DecryptMessage (General)** devuelve SEC I CONTEXT EXPIRED cuando el remitente del mensaje \_ ha cerrado la \_ \_ conexión. Para obtener información sobre cómo iniciar o reconocer un apagado, vea [Apagar una conexión Schannel.](shutting-down-an-schannel-connection.md)

Cuando se usa el SSP de Schannel, **DecryptMessage (General)** devuelve SEC \_ I \_ RENEGOTIATE cuando el remitente del mensaje desea volver a negociar la conexión (contexto [*de seguridad*](../secgloss/s-gly.md)). Una aplicación controla una renegociación solicitada llamando a [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (lado servidor) o [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) (lado cliente) y pasando búferes de entrada vacíos. Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión. Para obtener más información, vea [Creación de un contexto de seguridad de [*Schannel.*](../secgloss/s-gly.md)](creating-an-schannel-security-context.md)

Para obtener información sobre cómo interoperar con GSSAPI, vea [Interoperabilidad de SSPI/Kerberos con GSSAPI.](sspi-kerberos-interoperability-with-gssapi.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**EncryptMessage (general)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
