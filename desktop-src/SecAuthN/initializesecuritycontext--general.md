---
description: Inicia el contexto de seguridad de salida del lado [*cliente*](../secgloss/s-gly.md) desde un identificador de credenciales.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: Función InitializeSecurityContext (General, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: e0a4b1b9ff38faa840667f513aee25d61c23180d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567525"
---
# <a name="initializesecuritycontext-general-function"></a>Función InitializeSecurityContext (General)

La **función InitializeSecurityContext (General)** inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales. La función se usa para crear un contexto [*de seguridad entre*](../secgloss/s-gly.md) la aplicación cliente y un par remoto. **InitializeSecurityContext (General)** devuelve un token que el cliente debe pasar al elemento remoto del mismo nivel, que el mismo nivel envía a su vez a la implementación de seguridad local a través de la [**llamada AcceptSecurityContext (General).**](acceptsecuritycontext--general.md) Todos los autores de la llamada deben considerar opaco el token generado.

Normalmente, se **llama a la función InitializeSecurityContext (General)** en un bucle hasta que se establece un contexto de [*seguridad*](../secgloss/s-gly.md) suficiente.

Para obtener información sobre el uso de esta función con un proveedor [*de soporte técnico*](../secgloss/s-gly.md) de seguridad (SSP) específico, vea los temas siguientes.



| Tema                                                                                  | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)     | Inicia el contexto de [](../secgloss/s-gly.md) seguridad de salida del lado cliente desde un identificador de credenciales mediante el paquete de seguridad del proveedor de compatibilidad de seguridad de credenciales (CredSSP). [](../secgloss/s-gly.md)  
| [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)       | Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante el paquete de [*seguridad digest*](../secgloss/s-gly.md).                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante el paquete de [*seguridad*](../secgloss/s-gly.md)de Kerberos .                      |
| [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) | Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante el paquete de [*seguridad*](../secgloss/s-gly.md)Negotiate .                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante el paquete [*de*](../secgloss/s-gly.md)seguridad NTLM .                          |
| [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)   | Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante el paquete de seguridad de [*Schannel*](../secgloss/s-gly.md).                      |



 

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phCredential* \[ in, opcional\]
</dt> <dd>

Identificador de las credenciales [**devueltas por AcquireCredentialsHandle (general).**](acquirecredentialshandle--general.md) Este identificador se usa para compilar el contexto [*de seguridad*](../secgloss/s-gly.md). La **función InitializeSecurityContext (General)** requiere al menos credenciales OUTBOUND.

</dd> <dt>

*phContext* \[ in, opcional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (General),** este puntero es **NULL.** En la segunda llamada, este parámetro es un puntero al identificador al contexto con formato parcial devuelto en el *parámetro phNewContext* por la primera llamada.

Este parámetro es opcional con el Microsoft Digest SSP y se puede establecer en **NULL.**

Cuando se usa SSP de Schannel, en la primera llamada a **InitializeSecurityContext (General),** especifique **NULL.** En futuras llamadas, especifique el token recibido en el *parámetro phNewContext* después de la primera llamada a esta función.

</dd> <dt>

*pTargetName* \[ in, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL que indica el destino del contexto. El contenido de la cadena [*es específico del paquete*](../secgloss/s-gly.md) de seguridad, como se describe en la tabla siguiente. Esta lista no es exhaustiva. Los SSP del sistema adicionales y los SSP de terceros se pueden agregar a un sistema.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>SSP en uso</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Resumen</strong></dt><dt></dt> </dl></td><td>Cadena terminada en NULL que identifica de forma única el URI del recurso solicitado. La cadena debe estar compuesta de caracteres que se permiten en un URI y deben ser representables por el conjunto de código ASCII de EE. UU. La codificación por porcentaje se puede usar para representar caracteres fuera del conjunto de código ASCII de EE. UU.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos o Negotiate</strong></dt><dt></dt> </dl></td><td>Nombre de entidad de seguridad de servicio (SPN) o contexto [*de seguridad*](../secgloss/s-gly.md) del servidor de destino.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Nombre de entidad de seguridad de servicio (SPN) o contexto [*de seguridad*](../secgloss/s-gly.md) del servidor de destino.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>Schannel/SSL</strong></dt><dt></dt> </dl></td><td>Cadena terminada en NULL que identifica de forma única el servidor de destino. Schannel usa este valor para comprobar el certificado de servidor. Schannel también usa este valor para buscar la sesión en la caché de sesiones al restablecer una conexión. La sesión almacenada en caché solo se usa si se cumplen todas las condiciones siguientes:<ul><li>El nombre de destino es el mismo.</li><li>La entrada de caché no ha expirado.</li><li>El proceso de aplicación que llama a la función es el mismo.</li><li>La sesión de inicio de sesión es la misma.</li><li>El identificador de credenciales es el mismo.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*fContextReq* \[ En\]
</dt> <dd>

Marcas de bits que indican solicitudes para el contexto. No todos los paquetes pueden admitir todos los requisitos. Las marcas usadas para este parámetro tienen como prefijo ISC \_ REQ \_ , por ejemplo, ISC \_ REQ \_ DELEGATE. Este parámetro puede ser uno o varios de los siguientes marcadores de atributos.



<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>El [*paquete de seguridad*](../secgloss/s-gly.md) le asigna búferes de salida. Cuando haya terminado de usar los búferes de salida, puede liberarlos llamando a la función [<strong>FreeContextBuffer</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Cifre los mensajes mediante la función [<strong>EncryptMessage</strong>](encryptmessage--general.md).<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato. Este valor es el predeterminado para las delegaciones restringidas Kerberos, Negotiate [*y*](../secgloss/s-gly.md)NTLM.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>El servidor puede usar el contexto para autenticarse en otros servidores como el cliente. La ISC_REQ_MUTUAL_AUTH debe establecerse para que esta marca funcione. Válido para Kerberos. Ignore esta marca para [*la delegación restringida.*](../secgloss/c-gly.md)<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Cuando se producen errores, se notificará a la parte remota.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Use Digest para HTTP. Omita esta marca para usar Digest como un mecanismo SASL.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Firme mensajes y compruebe las firmas mediante las funciones [<strong>EncryptMessage</strong>](encryptmessage--general.md) y [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>Schannel no debe autenticar el servidor automáticamente.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Se cumple la directiva de autenticación mutua del servicio.<br/><blockquote>[!Caution]<br />
Esto no significa necesariamente que se realice la autenticación mutua, solo que se cumple la directiva de autenticación del servicio. Para asegurarse de que se realiza la autenticación mutua, llame a la función [<strong>QueryContextAttributes (General)</strong>](querycontextattributes--general.md).</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Si se establece esta marca, <strong>ISC_REQ_INTEGRITY</strong> se omite.<br/> Este valor solo es compatible con las delegaciones restringidas Negotiate [*y*](../secgloss/s-gly.md)Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Detecte los mensajes reproducido que se han codificado mediante las funciones [<strong>EncryptMessage</strong>](encryptmessage--general.md) o [<strong>MakeSignature</strong>](makesignature.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Detectar mensajes recibidos fuera de la secuencia.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Admite una conexión orientada a secuencias.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Se debe [*negociar una*](../secgloss/s-gly.md) nueva clave de sesión.<br/> Este valor solo es compatible con la delegación [*restringida de*](../secgloss/s-gly.md)Kerberos.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>Schannel no debe intentar proporcionar credenciales para el cliente automáticamente.<br/></td></tr></tbody></table>



 

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea *el parámetro pfContextAttr.*

Para obtener más descripciones de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

</dd> <dt>

*Reserved1* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*TargetDataRep* \[ En\]
</dt> <dd>

Representación de datos, como la ordenación de bytes, en el destino. Este parámetro puede ser SECURITY \_ NATIVE \_ DREP o SECURITY \_ NETWORK \_ DREP.

Este parámetro no se usa con Digest o Schannel. Esta establezca en cero.

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a los búferes proporcionados como entrada al paquete. A menos que el servidor haya iniciado el contexto de cliente, el valor de este parámetro debe ser **NULL** en la primera llamada a la función. En las llamadas posteriores a la función o cuando el servidor inició el contexto de cliente, el valor de este parámetro es un puntero a un búfer asignado con memoria suficiente para contener el token devuelto por el equipo remoto.

</dd> <dt>

*Reserved2* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (general),** este puntero recibe el nuevo identificador de contexto. En la segunda llamada, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

Al usar el SSP de Schannel, en las llamadas después de la primera llamada, pase el identificador devuelto aquí como parámetro *phContext* y especifique **NULL para** *phNewContext*.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a la [**estructura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recibe los datos de salida. Si se ha especificado un búfer como SEC \_ READWRITE en la entrada, estará ahí en la salida. El sistema asignará un búfer para el token de seguridad si se solicita (a través de ISC REQ ALLOCATE MEMORY) y rellenará la dirección en el descriptor del búfer para \_ \_ el token de \_ seguridad.

Cuando se usa Microsoft Digest SSP, este parámetro recibe la respuesta de desafío que se debe enviar al servidor.

Cuando se usa el SSP de Schannel, si se especifica la marca ALLOCATE MEMORY de ISC REQ, el SSP de Schannel asignará memoria para el búfer y colocará la información adecuada en \_ \_ \_ [**SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Además, el autor de la llamada debe pasar un búfer de tipo **SECBUFFER \_ ALERT.** En la salida, si se genera una alerta, este búfer contiene información sobre esa alerta y se produce un error en la función.

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntero a una variable para recibir un conjunto de marcas de bits que indican los [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) del contexto establecido. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

Las marcas usadas para este parámetro tienen el prefijo ISC \_ RET, como ISC \_ RET \_ DELEGATE. Para obtener una lista de valores válidos, vea el *parámetro fContextReq.*

No compruebe los atributos relacionados con la seguridad hasta que la llamada de función final se devuelva correctamente. Las marcas de atributo que no están relacionadas con la seguridad, como la marca ASC RET ALLOCATED MEMORY, se pueden comprobar \_ \_ antes de la \_ devolución final.

> [!Note]  
> Los atributos de contexto concretos pueden cambiar durante la negociación con un par remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el paquete [*de seguridad devuelva*](../secgloss/s-gly.md) siempre este valor en la hora local. Este parámetro es opcional y **se debe** pasar NULL para clientes de corta duración.

No hay ningún tiempo de expiración para Microsoft Digest o credenciales de seguridad [*de*](../secgloss/s-gly.md)SSP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve uno de los siguientes códigos de éxito.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC I COMPLETE AND CONTINUE (HE \_ \_ COMPLETADO Y \_ \_ CONTINUADO)**</dt> </dl> | El cliente debe llamar [**a CompleteAuthToken y,**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) a continuación, pasar la salida al servidor. A continuación, el cliente espera un token devuelto y lo pasa, en otra llamada, a [**InitializeSecurityContext (general).**](initializesecuritycontext--general.md)<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | El cliente debe terminar de compilar el mensaje y, a continuación, llamar a [**la función CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | El cliente debe enviar el token de salida al servidor y esperar un token de devolución. A continuación, el token devuelto se pasa en otra llamada a [**InitializeSecurityContext (general).**](initializesecuritycontext--general.md) El token de salida puede estar vacío.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**CREDENCIALES \_ \_ INCOMPLETAS DE SEC I \_**</dt> </dl> | Use con Schannel. El servidor ha solicitado la autenticación de cliente y las credenciales proporcionadas no incluyen un certificado o el certificado no lo emitió una entidad de certificación de confianza del servidor. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                              |
| <dl> <dt>**S \_ E \_ MENSAJE \_ INCOMPLETO**</dt> </dl>     | Use con Schannel. Los datos de todo el mensaje no se leyeron de la conexión.<br/> Cuando se devuelve este valor, el búfer *pInput* contiene una [**estructura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **miembro BufferType** de **SECBUFFER \_ MISSING.** El **miembro cbBuffer** de **SecBuffer** contiene un valor que indica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se realiza correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento evitando varias llamadas a esta función.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | El [*contexto de seguridad*](../secgloss/s-gly.md) se inicializó correctamente. No es necesario realizar otra [**llamada a InitializeSecurityContext (general).**](initializesecuritycontext--general.md) Si la función devuelve un token de salida, es decir, si secbuffer token en pOutput tiene una longitud distinta de cero, ese token debe enviarse \_ al servidor. <br/>                                                                                                                                                    |



 

Si se produce un error en la función, la función devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                          | Descripción                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>          | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERROR \_ INTERNO DE SEC E \_ \_**</dt> </dl>               | Error que no se ha asignado a un código de error SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**SEG \_ E \_ IDENTIFICADOR NO \_ VÁLIDO**</dt> </dl>               | El identificador pasado a la función no es válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E TOKEN NO \_ \_ VÁLIDO**</dt> </dl>                | El error se debe a un token de entrada con formato incorrecto, como un token dañado en tránsito, un token de tamaño incorrecto o un token pasado al paquete de seguridad [*incorrecto.*](../secgloss/s-gly.md) Pasar un token al paquete incorrecto puede ocurrir si el cliente y el servidor no negociaron el paquete [*de seguridad adecuado.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SE \_ DENEGÓ EL \_ INICIO DE SESIÓN \_ E.**</dt> </dl>                 | Error de inicio de sesión.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | No se pudo ponerse en contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría ser inaccesible o podría haber habido un error en la relación de confianza.<br/>                                                                                  |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>               | No hay credenciales disponibles en el [*paquete de seguridad*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEG \_ E \_ DESTINO \_ DESCONOCIDO**</dt> </dl>               | No se ha reconocido el destino.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNCIÓN NO \_ \_ ADMITIDA**</dt> </dl>         | Se especificó una marca de atributo de contexto que no es válida (ISC REQ DELEGATE o \_ \_ ISC \_ REQ PROMPT FOR CREDS) en el \_ \_ parámetro \_ *fContextReq.*<br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E ENTIDAD DE SEGURIDAD \_ \_ INCORRECTA**</dt> </dl>              | La entidad de seguridad que recibió la solicitud de autenticación no es la misma que la que se pasó al *parámetro pszTargetName.* Esto indica un error en la autenticación mutua.<br/>                                                                                                          |



 

## <a name="remarks"></a>Observaciones

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó confidencialidad, pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente.

Si los atributos del contexto [*de seguridad*](../secgloss/s-gly.md) no son suficientes, el cliente debe liberar el contexto creado parcialmente llamando a la [**función DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

Un **cliente usa la función InitializeSecurityContext (General)** para inicializar un contexto de salida.

Para un contexto de seguridad [*de dos etapas,*](../secgloss/s-gly.md)la secuencia de llamada es la siguiente:

1.  El cliente llama a la función con *phContext* establecido en **NULL** y rellena el descriptor del búfer con el mensaje de entrada.
2.  El [*paquete de seguridad*](../secgloss/s-gly.md) examina los parámetros y construye un token opaco, colocándolo en el elemento TOKEN de la matriz de búferes. Si el *parámetro fContextReq* incluye la marca ISC REQ ALLOCATE MEMORY, el paquete de seguridad asigna la memoria y devuelve el puntero en \_ el elemento \_ \_ TOKEN. [](../secgloss/s-gly.md)
3.  El cliente envía el token devuelto en el búfer *pOutput* al servidor de destino. A continuación, el servidor pasa el token como argumento de entrada en una llamada a la [**función AcceptSecurityContext (General).**](acceptsecuritycontext--general.md)
4.  [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) puede devolver un token, que el servidor envía al cliente para una segunda llamada a **InitializeSecurityContext (General)** si la primera llamada devolvió SEC \_ I CONTINUE \_ \_ NEEDED.

Para los contextos de [*seguridad de*](../secgloss/s-gly.md)varias etapas, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función como se describió anteriormente, pero el paquete devuelve el código de éxito SEC \_ I \_ CONTINUE \_ NEEDED.
2.  El cliente envía el token de salida al servidor y espera la respuesta del servidor.
3.  Tras la recepción de la respuesta del servidor, el cliente llama de nuevo a **InitializeSecurityContext (General),** con *phContext* establecido en el identificador que se devolvió de la última llamada. El token recibido del servidor se proporciona en el *parámetro pInput.*

Si el servidor ha respondido correctamente, el paquete [*de*](../secgloss/s-gly.md) seguridad devuelve SEC \_ E OK y se establece una sesión \_ segura.

Si la función devuelve una de las respuestas de error, no se acepta la respuesta del servidor y no se establece la sesión.

Si la función devuelve SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, se repiten los pasos \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 y 3.

Para inicializar [*un*](../secgloss/s-gly.md)contexto de seguridad, puede ser necesaria más de una llamada a esta función, en función del mecanismo de autenticación subyacente, así como de las opciones especificadas en el *parámetro fContextReq.*

Los *parámetros fContextReq* *y pfContextAttributes* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) El *parámetro pfContextAttributes* es válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto. Los resultados intermedios pueden establecer, por ejemplo, la marca \_ ISC RET \_ ALLOCATED \_ MEMORY.

Si se establece la marca CREDS USE SUPPLIED DE ISC REQ, el paquete de seguridad debe buscar un tipo de búfer \_ \_ \_ \_ SECBUFFER PKG PARAMS [](../secgloss/s-gly.md) en el búfer de entrada \_ \_ *pInput.* No se trata de una solución genérica, pero permite un emparejamiento seguro de [*paquetes*](../secgloss/s-gly.md) de seguridad y aplicaciones cuando sea necesario.

Si se especificó ISC REQ ALLOCATE MEMORY, el autor de la llamada debe liberar la memoria mediante \_ una llamada a la función \_ \_ [**FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Por ejemplo, el token de entrada podría ser el desafío de un administrador de LAN. En este caso, el token de salida sería la respuesta cifrada con NTLM al desafío.

La acción que realiza el cliente depende del código de retorno de esta función. Si el código devuelto es SEC E OK, no habrá ninguna segunda llamada \_ \_ a **InitializeSecurityContext (General)** y no se espera ninguna respuesta del servidor. Si el código devuelto es SEC I CONTINUE NEEDED, el cliente espera un token en respuesta del servidor y lo pasa en una segunda llamada \_ \_ a \_ **InitializeSecurityContext (General).** El código de retorno SEC I COMPLETE NEEDED indica que el cliente debe terminar de compilar el mensaje y \_ llamar a la función \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) El código SEC \_ I COMPLETE AND CONTINUE incorpora ambas \_ \_ \_ acciones.

Si **InitializeSecurityContext (General)** devuelve un resultado correcto en la primera (o solo) llamada, el autor de la llamada finalmente debe llamar a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) en el identificador devuelto, incluso si se produce un error en la llamada en una etapa posterior del intercambio de autenticación.

El cliente puede llamar a **InitializeSecurityContext (General)** de nuevo después de que se haya completado correctamente. Esto indica al paquete [*de seguridad que*](../secgloss/s-gly.md) se quiere una reauauticación.

Los llamadores del modo kernel tienen las siguientes diferencias: el nombre de destino es una cadena [*Unicode*](../secgloss/u-gly.md) que se debe asignar en la memoria virtual mediante [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); no se debe asignar desde el grupo. Los búferes pasados y proporcionados *en pInput* y *pOutput* deben estar en la memoria virtual, no en el grupo.

Al usar Schannel SSP, si la función devuelve SEC I INCOMPLETE CREDENTIALS, compruebe que especificó un certificado válido y de confianza \_ \_ en sus \_ credenciales. El certificado se especifica al llamar a la [**función AcquireCredentialsHandle (General).**](acquirecredentialshandle--general.md) El certificado debe ser un certificado de autenticación de cliente emitido por una entidad de certificación (CA) de confianza para el servidor. Para obtener una lista de las CA de confianza para el servidor, llame a la función [**QueryContextAttributes (General)**](querycontextattributes--general.md) y especifique el atributo SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.

Cuando se usa el SSP de Schannel, una vez que una aplicación cliente recibe un certificado de autenticación de una CA de confianza para el servidor, la aplicación crea una nueva credencial llamando a la función [**AcquireCredentialsHandle (General)**](acquirecredentialshandle--general.md) y, a continuación, llamando de nuevo a **InitializeSecurityContext (General),** especificando la nueva credencial en el *parámetro phCredential.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **InitializeSecurityContextW** (Unicode) e **InitializeSecurityContextA** (ANSI)<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**AcquireCredentialsHandle (General)**](acquirecredentialshandle--general.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
