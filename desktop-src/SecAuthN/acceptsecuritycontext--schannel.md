---
description: Habilita el componente de servidor de una aplicación de transporte para establecer un [*contexto de seguridad*](../secgloss/s-gly.md) entre el servidor y un cliente remoto que usa Schannel.
ms.assetid: 03fd5272-8476-4c93-8590-0d00acf6a130
title: Función AcceptSecurityContext (Schannel) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: ba353cfbe64d6471230a720680301ebab0da511a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720559"
---
# <a name="acceptsecuritycontext-schannel-function"></a>AcceptSecurityContext (Schannel) (función)

La función **AcceptSecurityContext (Schannel)** permite al componente de servidor de una aplicación de transporte establecer un [*contexto de seguridad*](../secgloss/s-gly.md) entre el servidor y un cliente remoto. El cliente remoto utiliza la función [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) para iniciar el proceso de establecer un [*contexto de seguridad*](../secgloss/s-gly.md). El servidor puede requerir uno o más tokens de respuesta del cliente remoto para completar el establecimiento del [*contexto de seguridad*](../secgloss/s-gly.md).

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

*phCredential* \[ en, opcional\]
</dt> <dd>

Identificador de las credenciales del servidor. El servidor llama a la función [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) con el marcador de SECPKG \_ CRED \_ entrante o SECPKG \_ CRED \_ ambos establecidos para recuperar este identificador.

</dd> <dt>

*phContext* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **AcceptSecurityContext (Schannel)**, este puntero es **null**. En las llamadas posteriores, *phContext* es el identificador del contexto parcialmente formado que se devolvió en el parámetro *phNewContext* por la primera llamada.

</dd> <dt>

*pInput* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generada por una llamada de cliente a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) que contiene el descriptor de búfer de entrada.

Al usar el [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) de Schannel (SSP), el primer búfer debe ser del tipo SECBUFFER \_ token y contener el token de seguridad recibido del cliente. El segundo búfer debe ser de tipo SECBUFFER \_ vacío.

</dd> <dt>

*fContextReq* \[ de\]
</dt> <dd>

Marcas de bits que especifican los atributos requeridos por el servidor para establecer el contexto. **Las marcas de bits** se pueden combinar mediante operaciones OR bit a bit. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                         | Significado                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASC_REQ_ALLOCATE_MEMORY"></span><span id="asc_req_allocate_memory"></span><dl> <dt>**ASC \_ req \_ asignar \_ memoria**</dt> </dl> | Digest y Schannel asignarán los búferes de salida automáticamente. Cuando haya terminado de usar los búferes de salida, liberelos mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/> |
| <span id="ASC_REQ_CONFIDENTIALITY"></span><span id="asc_req_confidentiality"></span><dl> <dt>**\_confidencialidad de REQ. \_**</dt> </dl>  | Cifrar y descifrar mensajes.<br/> El SSP de síntesis solo admite esta marca para SASL.<br/>                                                                                                    |
| <span id="ASC_REQ_CONNECTION"></span><span id="asc_req_connection"></span><dl> <dt>**\_conexión de REQ de ASC \_**</dt> </dl>                 | El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato.<br/>                                                                                                                                    |
| <span id="ASC_REQ_EXTENDED_ERROR"></span><span id="asc_req_extended_error"></span><dl> <dt>**\_error de solicitud \_ EXTENDIda ASC \_**</dt> </dl>    | Cuando se produzcan errores, se notificará a la parte remota.<br/>                                                                                                                                        |
| <span id="ASC_REQ_MUTUAL_AUTH"></span><span id="asc_req_mutual_auth"></span><dl> <dt>**\_ \_ autenticación mutua de \_ req**</dt> </dl>             | El cliente debe proporcionar un certificado que se usará para la autenticación del cliente.<br/>                                                                                                         |
| <span id="ASC_REQ_REPLAY_DETECT"></span><span id="asc_req_replay_detect"></span><dl> <dt>**\_detección de \_ repeticiones de ASC req \_**</dt> </dl>       | Detectar paquetes reproducidos.<br/>                                                                                                                                                                     |
| <span id="ASC_REQ_SEQUENCE_DETECT"></span><span id="asc_req_sequence_detect"></span><dl> <dt>**\_detección de \_ secuencia de REQ de ASC \_**</dt> </dl> | Detecta mensajes recibidos de la secuencia.<br/>                                                                                                                                                    |
| <span id="ASC_REQ_STREAM"></span><span id="asc_req_stream"></span><dl> <dt>**\_flujo de REQ de ASC \_**</dt> </dl>                             | Admitir una conexión orientada a flujos.<br/> Esta marca solo es compatible con Schannel.<br/>                                                                                                    |



 

Para ver posibles marcas de atributo y su significado, vea [requisitos de contexto](context-requirements.md). Las marcas usadas para este parámetro llevan el prefijo ASC \_ req, por ejemplo, \_ el \_ delegado de REQ.

Es posible que el cliente no admita los atributos solicitados. Para obtener más información, consulte el parámetro *pfContextAttr* .

</dd> <dt>

*TargetDataRep* \[ de\]
</dt> <dd>

Este parámetro no se utiliza con Schannel. Especifique cero para este parámetro.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **AcceptSecurityContext (Schannel)**, este puntero recibe el nuevo identificador de contexto. En las llamadas posteriores, *phNewContext* puede ser el mismo que el identificador especificado en el parámetro *phContext* .

</dd> <dt>

*pOutput* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene el descriptor del búfer de salida. Este búfer se envía al cliente para la entrada en llamadas adicionales a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md). Se puede generar un búfer de salida aunque la función devuelva SEC \_ E \_ Aceptar. Cualquier búfer generado debe volver a enviarse a la aplicación cliente.

En la salida, este búfer recibe un token para el [*contexto de seguridad*](../secgloss/s-gly.md). El token se debe enviar al cliente. La función también puede devolver un búfer de tipo SECBUFFER \_ extra. Además, el llamador debe pasar un búfer de tipo **SECBUFFER \_ Alert**. En la salida, si se genera una alerta, este búfer contiene información sobre esa alerta y se produce un error en la función.

</dd> <dt>

*pfContextAttr* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un conjunto de marcadores de bits que indican los atributos del contexto establecido. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md). Las marcas usadas para este parámetro tienen el prefijo ASC \_ RET, por ejemplo, el delegado de ASC \_ RET \_ .

No Compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo no relacionadas con la seguridad, como \_ la \_ marca ASC RET asignado \_ memoria, se pueden comprobar antes de la devolución final.

</dd> <dt>

*ptsTimeStamp* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora de expiración del contexto. Se recomienda que el [*paquete de seguridad*](../secgloss/s-gly.md) devuelva siempre este valor en la hora local.

Esto es opcional cuando se usa el SSP de Schannel. Cuando la parte remota ha proporcionado un certificado que se va a utilizar para la autenticación, este parámetro recibe la hora de expiración de ese certificado. Si no se ha proporcionado ningún certificado, se devuelve un valor de tiempo máximo.

> [!Note]  
> Hasta la última llamada del proceso de autenticación, la hora de expiración del contexto puede ser incorrecta porque se proporcionará más información en las fases posteriores de la negociación. Por lo tanto, *ptsTimeStamp* debe ser **null** hasta la última llamada a la función.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Código o valor devuelto</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><dl> <dt><strong>SEC_E_INCOMPLETE_MESSAGE</strong></dt> <dt>0x80090318L</dt> </dl></td><td>La función se ha realizado correctamente. Los datos del búfer de entrada están incompletos. La aplicación debe leer datos adicionales del cliente y llamar de nuevo a [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/> Cuando se devuelve este valor, el búfer <em>pInput</em> contiene una estructura [<strong>SecBuffer</strong>] (/Windows/Win32/API/SSPI/NS-SSPI-secbuffer) con un miembro <strong>BufferType</strong> de <strong>SECBUFFER_MISSING</strong>. El miembro <strong>cbBuffer</strong> de <strong>SecBuffer</strong> contiene un valor que indica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se ejecute correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento al evitar varias llamadas a esta función.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INSUFFICIENT_MEMORY</strong></dt> <dt>0x80090300L</dt> </dl></td><td>Error en la función. No hay suficiente memoria disponible para completar la acción solicitada.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INTERNAL_ERROR</strong></dt> <dt>0x80090304L</dt> </dl></td><td>Error en la función. Error que no se ha asignado a un código de error SSPI.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_INVALID_HANDLE</strong></dt> <dt>0x80100003L</dt> </dl></td><td>Error en la función. El identificador pasado a la función no es válido.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_INVALID_TOKEN</strong></dt> <dt>0x80090308L</dt> </dl></td><td>Error en la función. El token que se ha pasado a la función no es válido.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_LOGON_DENIED</strong></dt> <dt>0x8009030CL</dt> </dl></td><td>Error de inicio de sesión.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_NO_AUTHENTICATING_AUTHORITY</strong></dt> <dt>0x80090311L</dt> </dl></td><td>Error en la función. No se pudo establecer contacto con ninguna autoridad para la autenticación. Esto puede deberse a las siguientes condiciones:<br/><ul><li>El nombre de dominio de la entidad de autenticación no es correcto.</li><li>El dominio no está disponible.</li><li>Error en la relación de confianza.</li></ul></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_NO_CREDENTIALS</strong></dt> <dt>0x8009030EL</dt> </dl></td><td>Error en la función. El identificador de credenciales especificado en el parámetro <em>phCredential</em> no es válido. Este valor se puede devolver cuando se usa la síntesis o el SSP de Schannel.<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_OK</strong></dt> <dt>0x00000000L</dt> </dl></td><td>La función se ha realizado correctamente. Se aceptó el [*contexto de seguridad*](../secgloss/s-gly.md) recibido del cliente. Si la función generó un token de salida, se debe enviar al proceso del cliente.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_E_UNSUPPORTED_FUNCTION</strong></dt> <dt>0x80090302L</dt> </dl></td><td>Error en la función. Se especificó una marca de atributo de contexto que no es válida (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) en el parámetro <em>fContextReq</em> .<br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_E_APPLICATION_PROTOCOL_MISMATCH</strong></dt> <dt>0x80090367L</dt> </dl></td><td>No existe ningún protocolo de aplicación común entre el cliente y el servidor.<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_COMPLETE_AND_CONTINUE</strong></dt> <dt>0x00090314L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe llamar a [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken) y pasar el token de salida al cliente. Después, el servidor espera un token de devolución del cliente y, a continuación, realiza otra llamada a [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD). <br/></td></tr><tr class="odd"><td><dl> <dt><strong>SEC_I_COMPLETE_NEEDED</strong></dt> <dt>0x00090313L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe terminar de compilar el mensaje desde el cliente y, a continuación, llamar a la función [<strong>CompleteAuthToken</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-completeauthtoken).<br/></td></tr><tr class="even"><td><dl> <dt><strong>SEC_I_CONTINUE_NEEDED</strong></dt> <dt>0x00090312L</dt> </dl></td><td>La función se ha realizado correctamente. El servidor debe enviar el token de salida al cliente y esperar un token devuelto. El token devuelto se debe pasar en <em>pInput</em> para otra llamada a [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD).<br/></td></tr><tr class="odd"><td><dl> <dt><strong>STATUS_LOGON_FAILURE</strong></dt> <dt>0xC000006DL</dt> </dl></td><td>Error en la función. Se llamó a la función [<strong>AcceptSecurityContext (Schannel)</strong>] (AcceptSecurityContext--Schannel.MD) después de establecer el contexto especificado. Este valor se puede devolver cuando se usa el SSP de síntesis.<br/></td></tr></tbody></table>



 

## <a name="remarks"></a>Observaciones

La función **AcceptSecurityContext (Schannel)** es el homólogo del servidor para la función [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) .

Cuando el servidor recibe una solicitud de un cliente, el servidor usa el parámetro *fContextReq* para especificar lo que requiere de la sesión. De este modo, un servidor puede especificar que los clientes deben ser capaces de usar una sesión confidencial o comprobada por [*integridad*](../secgloss/i-gly.md), y puede rechazar clientes que no puedan satisfacer esa demanda. Como alternativa, un servidor no puede necesitar nada y lo que el cliente puede proporcionar o requiera se devuelve en el parámetro *pfContextAttr* .

Para un paquete que admite la autenticación de varios tramos, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente transmite un token al servidor.
2.  El servidor llama a **AcceptSecurityContext (Schannel)** la primera vez, que genera un token de respuesta que se envía al cliente.
3.  El cliente recibe el token y lo pasa a [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md). Si **InitializeSecurityContext (Schannel)** devuelve sec \_ e \_ OK, se ha completado la autenticación mutua y se puede iniciar una sesión segura. Si **InitializeSecurityContext (Schannel)** devuelve un código de error, finaliza la negociación de la autenticación mutua. De lo contrario, el token de seguridad devuelto por **InitializeSecurityContext (Schannel)** se envía al cliente y se repiten los pasos 2 y 3.

Los parámetros *fContextReq* y *pfContextAttr* son máscaras de texto que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

> [!Note]  
> El parámetro *pfContextAttr* es válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto. Las devoluciones intermedias se pueden establecer, por ejemplo, la \_ \_ marca de memoria asignada de ISC \_ .

 

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó la confidencialidad (cifrado), pero no se pudo establecer, algunas aplicaciones pueden optar por cerrar la conexión inmediatamente. Si no se puede establecer el [*contexto de seguridad*](../secgloss/s-gly.md) , el servidor debe liberar el contexto creado parcialmente mediante una llamada a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Para obtener información sobre cuándo se debe llamar a la función **DeleteSecurityContext** , vea **DeleteSecurityContext**.

Una vez establecido el [*contexto de seguridad*](../secgloss/s-gly.md) , la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar un identificador de la cuenta de usuario a la que se asignó el certificado de cliente. Además, el servidor puede usar la función [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar al usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
</dt> </dl>

 

 
