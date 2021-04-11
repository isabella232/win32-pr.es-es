---
description: Descifra un mensaje.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: DecryptMessage (general) (función) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275628"
---
# <a name="decryptmessage-general-function"></a>DecryptMessage (general), función

La función **DecryptMessage (general)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.

El [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) implícita (SSP) proporciona confidencialidad de cifrado y descifrado para los mensajes intercambiados entre el cliente y el servidor como un mecanismo SASL únicamente.

Esta función también se usa con el SSP de Schannel para indicar una solicitud del remitente de un mensaje para una renegociación (Redo) de los atributos de conexión o para un cierre de la conexión.

> [!Note]  
> Se puede llamar a [**EncryptMessage (general)**](encryptmessage--general.md) y **DecryptMessage (general)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

 

Para obtener información sobre el uso de esta función con un SSP específico, vea los temas siguientes.



| Tema                                                            | Descripción                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (Resumen)**](decryptmessage--digest.md)       | Descifra un mensaje mediante el uso de Digest.    |
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

*phContext* \[ de\]
</dt> <dd>

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para descifrar el mensaje.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos puede ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.

Al usar el SSP de síntesis, en la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos debe ser de tipo SECBUFFER \_ Data o SECBUFFER \_ Stream y debe contener el mensaje cifrado.

Cuando se usa Schannel SSP con contextos que no están orientados a la conexión, en la entrada, la estructura debe contener cuatro estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Exactamente un búfer debe ser de tipo SECBUFFER \_ y contener un mensaje cifrado, que se descifra en su lugar. Los búferes restantes se utilizan para la salida y deben ser de tipo SECBUFFER \_ vacío. En el caso de los contextos orientados a la conexión, \_ se debe proporcionar un búfer de tipo de datos SECBUFFER, como se indica para los contextos no orientados a la conexión. Además, \_ también se debe proporcionar un segundo búfer de tipo de token de SECBUFFER que contenga un token de seguridad.

</dd> <dt>

*MessageSeqNo* \[ de\]
</dt> <dd>

El número de secuencia esperado por la aplicación de transporte, si existe. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.

Al usar el SSP de síntesis, este parámetro debe establecerse en cero. El SSP de síntesis administra la numeración de secuencias internamente.

Cuando se usa Schannel SSP, este parámetro debe establecerse en cero. Schannel SSP no utiliza números de secuencia.

</dd> <dt>

*pfQOP* \[ enuncia\]
</dt> <dd>

Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.

Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.

Este parámetro puede ser una de las marcas siguientes.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>No se cifró el mensaje, pero se produjo un encabezado o un finalizador.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Al usar el SSP de síntesis, use esta marca cuando el [*contexto de seguridad*](../secgloss/s-gly.md) esté establecido para comprobar solo la [*firma*](../secgloss/s-gly.md) . Para obtener más información, consulte [Quality of Protection](quality-of-protection.md).<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**búfer de s \_ E s \_ \_ demasiado \_ pequeño**</dt> </dl>      | El búfer de mensajes es demasiado pequeño. Se usa con el SSP de síntesis.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ \_ sistema criptográfico \_ no válido**</dt> </dl> | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) . Se usa con el SSP de síntesis.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ mensaje incompleto \_**</dt> </dl>     | Los datos del búfer de entrada están incompletos. La aplicación debe leer más datos del servidor y llamar de nuevo a [**DecryptMessage (general)**](decryptmessage--general.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ identificador no válido \_**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* . Se usa con los SSP de síntesis y Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ token no válido \_**</dt> </dl>          | Los búferes son del tipo incorrecto o no se encontró ningún búfer de tipo SECBUFFER \_ datos. Se usa con el SSP de Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ mensaje \_ modificado**</dt> </dl>        | El mensaje se ha modificado. Se usa con los SSP de síntesis y Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ fuera \_ de \_ secuencia**</dt> </dl>       | No se recibió el mensaje en la secuencia correcta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ QOP \_ no \_ admitidos**</dt> </dl>     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md). Se usa con el SSP de síntesis.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ I en \_ contexto \_ expirado**</dt> </dl>        | El remitente del mensaje ha terminado de usar la conexión y ha iniciado un cierre. Para obtener información acerca de cómo iniciar o reconocer un cierre, vea [apagar una conexión Schannel](shutting-down-an-schannel-connection.md). Se usa con el SSP de Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ I \_ renegotiate**</dt> </dl>             | La parte remota requiere una nueva secuencia de protocolo de enlace o la aplicación acaba de iniciar un cierre. Vuelva al bucle de negociación y llame a [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) o a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md), pasando los búferes de entrada vacíos. <br/> Si la función devuelve un búfer de tipo **s de \_ búfer \_ adicional**, se debe pasar a la función [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) como un búfer de entrada.<br/> Se usa con el SSP de Schannel.<br/> No se admite la renegociación para el modo de kernel Schannel. El autor de la llamada debe omitir este valor devuelto o cerrar la conexión. Si se omite el valor, puede que el cliente o el servidor cierren la conexión como resultado.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando se usa Schannel SSP, la función **DecryptMessage (general)** devuelve la \_ hora en que se \_ ha agotado el contexto I en que \_ el remitente del mensaje ha cerrado la conexión. Para obtener información acerca de cómo iniciar o reconocer un cierre, vea [apagar una conexión Schannel](shutting-down-an-schannel-connection.md).

Cuando se usa Schannel SSP, **DecryptMessage (general)** devuelve s \_ que se \_ renegocian cuando el remitente del mensaje desea volver a negociar la conexión ([*contexto de seguridad*](../secgloss/s-gly.md)). Una aplicación controla una renegociación solicitada mediante una llamada a [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) (el lado servidor) o a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) (cliente) y al pasar búferes de entrada vacíos. Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión. Para obtener más información, vea [crear un [*contexto de seguridad*](../secgloss/s-gly.md)de Schannel](creating-an-schannel-security-context.md).

Para obtener información acerca de cómo interoperar con GSSAPI, consulte [interoperabilidad de SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**EncryptMessage (general)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
