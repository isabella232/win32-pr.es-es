---
description: Permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad [*entre*](../secgloss/s-gly.md) el servidor y un cliente remoto que usa Negotiate.
ms.assetid: aaec6fee-df6b-4033-8ece-73ecd1799653
title: Función AcceptSecurityContext (Negotiate) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13aa91545e5301e10a1f9d36e93e2d4995c15253
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567553"
---
# <a name="acceptsecuritycontext-negotiate-function"></a>Función AcceptSecurityContext (Negotiate)

La **función AcceptSecurityContext (Negotiate)** permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad [*entre*](../secgloss/s-gly.md) el servidor y un cliente remoto. El cliente remoto usa la [**función InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) para iniciar el proceso de establecimiento de un contexto [*de seguridad*](../secgloss/s-gly.md). El servidor puede requerir uno o varios tokens de respuesta del cliente remoto para completar el establecimiento del [*contexto de seguridad*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_Entry AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _Inout_opt_ PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          fContextReq,
  _In_        ULONG          TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsTimeStamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phCredential* \[ in, opcional\]
</dt> <dd>

Identificador de las credenciales del servidor. El servidor llama a [**la función AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md) con la marca SECPKG CRED INBOUND o \_ SECPKG CRED BOTH establecida para \_ recuperar este \_ \_ identificador.

</dd> <dt>

*phContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (Negotiate),** este puntero es **NULL.** En las llamadas posteriores, *phContext* es el identificador del contexto con formato parcial que la primera llamada devolvió en el parámetro *phNewContext.*

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generada por una llamada de cliente a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) que contiene el descriptor del búfer de entrada.

La información de enlace de canal se puede especificar pasando una estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo **SECBUFFER \_ CHANNEL \_ BINDINGS** además de los búferes generados por la llamada a la función [**InitializeSecurityContext (General).**](initializesecuritycontext--general.md) La información de enlace de canal para el búfer de enlace de canal se puede obtener llamando a la función [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) en el contexto Schannel que el cliente usó para autenticarse.

</dd> <dt>

*fContextReq* \[ En\]
</dt> <dd>

Marcas de bits que especifican los atributos requeridos por el servidor para establecer el contexto. Las marcas de bits se pueden combinar mediante operaciones **OR** bit a bit. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                         | Significado                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**CONFIDENCIALIDAD DE ASC \_ REQ \_**</dt> </dl>  | Cifrar y descifrar mensajes.<br/>                                                                                                                                                                                   |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**CONEXIÓN DE ASC \_ \_ REQ**</dt> </dl>                 | El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato.<br/>                                                                                                                                                       |
| <span id="ASC_REQ_DELEGATE"></span><span id="asc_req_delegate"></span><dl> <dt>**ASC \_ REQ \_ DELEGATE**</dt> </dl>                       | El servidor puede suplantar al cliente. Válido para Kerberos. Ignore esta marca para [*la delegación restringida.*](../secgloss/c-gly.md)<br/> |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**ERROR EXTENDIDO DE ASC \_ REQ \_ \_**</dt> </dl>    | Cuando se producen errores, se notificará a la parte remota.<br/>                                                                                                                                                           |
| <span id="ASC_REQ_INTEGRITY"></span><span id="asc_req_integrity"></span><dl> <dt>**INTEGRIDAD DE ASC \_ REQ \_**</dt> </dl>                    | Firmar mensajes y comprobar firmas.<br/>                                                                                                                                                                            |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**ASC \_ REQ \_ REPLAY \_ DETECT**</dt> </dl>       | Detectar paquetes reproducido.<br/>                                                                                                                                                                                        |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**ASC \_ REQ \_ SEQUENCE \_ DETECT**</dt> </dl> | Detectar mensajes recibidos fuera de la secuencia.<br/>                                                                                                                                                                       |



 

Para ver las posibles marcas de atributo y sus significados, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen como prefijo ASC \_ REQ, por ejemplo, ASC \_ REQ \_ DELEGATE.

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea *el parámetro pfContextAttr.*

</dd> <dt>

*TargetDataRep* \[ En\]
</dt> <dd>

Representación de datos, como la ordenación de bytes, en el destino. Este parámetro puede ser SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (Negotiate),** este puntero recibe el nuevo identificador de contexto. En las llamadas posteriores, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene el descriptor del búfer de salida. Este búfer se envía al cliente para su entrada en llamadas adicionales a [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Se puede generar un búfer de salida incluso si la función devuelve SEC \_ E \_ OK. Cualquier búfer generado debe devolverse a la aplicación cliente.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un conjunto de marcas de bits que indican los atributos del contexto establecido. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen el prefijo ASC \_ RET, por ejemplo, ASC \_ RET \_ DELEGATE.

No compruebe los atributos relacionados con la seguridad hasta que la llamada de función final se devuelva correctamente. Las marcas de atributo no relacionadas con la seguridad, como la marca ASC RET ALLOCATED MEMORY, se pueden comprobar \_ \_ antes de la \_ devolución final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el [*paquete de seguridad*](../secgloss/s-gly.md) devuelva siempre este valor en la hora local.

> [!Note]  
> Hasta la última llamada del proceso de autenticación, la hora de expiración del contexto puede ser incorrecta porque se proporciona más información durante las fases posteriores de la negociación. Por lo tanto, *ptsTimeStamp* debe ser **NULL hasta** la última llamada a la función.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Código o valor devuelto</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Error en la función. No hay suficiente memoria disponible para completar la acción solicitada.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Error en la función. Error que no se ha asignado a un código de error SSPI.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Error en la función. El identificador pasado a la función no es válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Error en la función. El token pasado a la función no es válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Error de inicio de sesión.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Error en la función. No se pudo ponerse en contacto con ninguna autoridad para la autenticación. Esto podría deberse a las condiciones siguientes:<br/><ul><li>El nombre de dominio de la entidad de autenticación es incorrecto.</li><li>El dominio no está disponible.</li><li>Error en la relación de confianza.</li></ul></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>La función se ha realizado correctamente. Se [*aceptó*](../secgloss/s-gly.md) el contexto de seguridad recibido del cliente. Si la función generó un token de salida, se debe enviar al proceso de cliente.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe llamar a [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y pasar el token de salida al cliente. A continuación, el servidor espera un token de devolución del cliente y, a continuación, realiza otra llamada a [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe terminar de compilar el mensaje desde el cliente y, a continuación, llamar a la función [<strong>CompleteAuthToken</strong>](/windows/win32/api/sspi/nf-sspi-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe enviar el token de salida al cliente y esperar un token devuelto. El token devuelto debe pasarse en <em>pInput para</em> otra llamada a [<strong>AcceptSecurityContext (Negotiate)</strong>](acceptsecuritycontext--negotiate.md).<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Observaciones

La **función AcceptSecurityContext (Negotiate)** es el homólogo del servidor de [**la función InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md)

Cuando el servidor recibe una solicitud de un cliente, el servidor usa el parámetro *fContextReq* para especificar lo que requiere de la sesión. De este modo, un servidor puede especificar que los [](../secgloss/i-gly.md)clientes deben ser capaces de usar una sesión confidencial o comprobada por integridad, y puede rechazar clientes que no puedan satisfacer esa demanda. Como alternativa, un servidor no puede requerir nada y lo que el cliente pueda proporcionar o requiera se devuelve en el *parámetro pfContextAttr.*

Para un paquete que admite la autenticación de varios pasos, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente transmite un token al servidor.
2.  El servidor llama **a AcceptSecurityContext (Negotiate)** la primera vez, lo que genera un token de respuesta que se envía al cliente.
3.  El cliente recibe el token y lo pasa a [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md) Si **InitializeSecurityContext (Negotiate)** devuelve SEC E OK, se ha completado la autenticación mutua y se puede iniciar \_ una sesión \_ segura. Si **InitializeSecurityContext (Negotiate)** devuelve un código de error, finaliza la negociación de autenticación mutua. De lo contrario, el token de seguridad devuelto por **InitializeSecurityContext (Negotiate)** se envía al cliente y se repiten los pasos 2 y 3.

Los *parámetros fContextReq* y *pfContextAttr* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

> [!Note]  
> El *parámetro pfContextAttr es* válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas relativas a los aspectos de seguridad del contexto. Los resultados intermedios pueden establecer, por ejemplo, la marca \_ ISC RET \_ ALLOCATED \_ MEMORY.

 

El autor de la llamada es responsable de determinar si los atributos de contexto final son suficientes. Si, por ejemplo, se solicitó confidencialidad (cifrado), pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente. Si no [*se puede establecer el*](../secgloss/s-gly.md) contexto de seguridad, el servidor debe liberar el contexto creado parcialmente llamando a la función [**DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Para obtener información sobre cuándo llamar a **la función DeleteSecurityContext,** vea **DeleteSecurityContext**.

Una vez [*establecido el contexto*](../secgloss/s-gly.md) de seguridad, la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar un identificador de la cuenta de usuario a la que se ha asignado el certificado de cliente. Además, el servidor puede usar la [**función ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar al usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> </dl>

 

 
