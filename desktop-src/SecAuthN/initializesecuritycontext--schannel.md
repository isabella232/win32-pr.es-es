---
description: Inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales mediante la delegación restringida [*de Schannel*](../secgloss/s-gly.md).
ms.assetid: c451089a-d10d-469c-99dd-43d75a6b0b2a
title: Función InitializeSecurityContext (Schannel) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 29bbaeac3ef307e3ef846f526d96a98a22395742
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472911"
---
# <a name="initializesecuritycontext-schannel-function"></a>Función InitializeSecurityContext (Schannel)

La **función InitializeSecurityContext (Schannel)** inicia el contexto de seguridad de salida del lado cliente [*desde*](../secgloss/s-gly.md) un identificador de credenciales. La función se usa para crear un contexto [*de seguridad entre*](../secgloss/s-gly.md) la aplicación cliente y un par remoto. **InitializeSecurityContext (Schannel)** devuelve un token que el cliente debe pasar al elemento remoto del mismo nivel, que el mismo nivel envía a su vez a la implementación de seguridad local a través de la llamada [**AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Todos los autores de la llamada deben considerar opaco el token generado.

Normalmente, se **llama a la función InitializeSecurityContext (Schannel)** en un bucle hasta que se establece un contexto [*de*](../secgloss/s-gly.md) seguridad suficiente.

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

Identificador de las credenciales [**devueltas por AcquireCredentialsHandle (Schannel).**](acquirecredentialshandle--schannel.md) Este identificador se usa para compilar el contexto [*de seguridad*](../secgloss/s-gly.md). La **función InitializeSecurityContext (Schannel)** requiere al menos credenciales OUTBOUND.

</dd> <dt>

*phContext* \[ in, opcional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (Schannel),** este puntero es **NULL.** En la segunda llamada, este parámetro es un puntero al identificador al contexto parcialmente formado devuelto en el *parámetro phNewContext* por la primera llamada.

En la primera llamada a **InitializeSecurityContext (Schannel),** especifique **NULL.** En futuras llamadas, especifique el token recibido en el *parámetro phNewContext* después de la primera llamada a esta función.

</dd> <dt>

*pszTargetName* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica de forma única el servidor de destino. Schannel usa este valor para comprobar el certificado de servidor. Schannel también usa este valor para buscar la sesión en la caché de sesiones al restablecer una conexión. La sesión almacenada en caché solo se usa si se cumplen todas las condiciones siguientes:

-   El nombre de destino es el mismo.
-   La entrada de caché no ha expirado.
-   El proceso de aplicación que llama a la función es el mismo.
-   La sesión de inicio de sesión es la misma.
-   El identificador de credenciales es el mismo.

</dd> <dt>

*fContextReq* \[ En\]
</dt> <dd>

Marcas de bits que indican solicitudes para el contexto. No todos los paquetes pueden admitir todos los requisitos. Las marcas usadas para este parámetro tienen como prefijo ISC \_ REQ \_ , por ejemplo, ISC \_ REQ \_ DELEGATE. Este parámetro puede ser uno o varios de los siguientes marcadores de atributos.




| Valor | Significado | 
|-------|---------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl><dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt></dl> | El [*paquete de seguridad*](../secgloss/s-gly.md) le asigna búferes de salida. Cuando haya terminado de usar los búferes de salida, puede liberarlos llamando a la [<strong>función FreeContextBuffer.</strong>](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br /> | 
| <span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl><dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt></dl> | Cifre los mensajes mediante la [<strong>función EncryptMessage.</strong>](encryptmessage--general.md)<br /> | 
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl><dt><strong>ISC_REQ_CONNECTION</strong></dt></dl> | El [*contexto de seguridad*](../secgloss/s-gly.md) no controlará los mensajes de formato.<br /> | 
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl><dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt></dl> | Cuando se producen errores, se notificará a la parte remota.<br /> | 
| <span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl><dt><strong>ISC_REQ_INTEGRITY</strong></dt></dl> | Firmar mensajes y comprobar firmas mediante las [<strong>funciones EncryptMessage</strong>](encryptmessage--general.md) y [<strong>MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl><dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt></dl> | Schannel no debe autenticar el servidor automáticamente.<br /> | 
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl><dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt></dl> | Se cumple la directiva de autenticación mutua del servicio.<br /><blockquote>[!Caution]<br />Esto no significa necesariamente que se realice la autenticación mutua, solo que se cumple la directiva de autenticación del servicio. Para asegurarse de que se realiza la autenticación mutua, llame a [<strong>la función QueryContextAttributes (Schannel).</strong>](querycontextattributes--schannel.md)</blockquote><br /> | 
| <span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl><dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt></dl> | Detecte los mensajes reproducido que se han codificado mediante las [<strong>funciones EncryptMessage</strong>](encryptmessage--general.md) [<strong>o MakeSignature.</strong>](makesignature.md)<br /> | 
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl><dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt></dl> | Detectar mensajes recibidos fuera de la secuencia.<br /> | 
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl><dt><strong>ISC_REQ_STREAM</strong></dt></dl> | Admite una conexión orientada a secuencias.<br /> | 
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl><dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt></dl> | Schannel no debe intentar proporcionar credenciales para el cliente automáticamente.<br /> | 




 

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea *el parámetro pfContextAttr.*

Para obtener más descripciones de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

</dd> <dt>

*Reserved1* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*TargetDataRep* \[ En\]
</dt> <dd>

Este parámetro no se usa con Schannel. Esta establezca en cero.

</dd> <dt>

*pInput* \[ in, opcional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a los búferes proporcionados como entrada al paquete. A menos que el servidor haya iniciado el contexto de cliente, el valor de este parámetro debe ser **NULL** en la primera llamada a la función. En las llamadas posteriores a la función o cuando el servidor inició el contexto de cliente, el valor de este parámetro es un puntero a un búfer asignado con memoria suficiente para contener el token devuelto por el equipo remoto.

En las llamadas a esta función después de la llamada inicial, debe haber dos búferes. El primero tiene el tipo **\_ SECBUFFER TOKEN** y contiene el token recibido del servidor. El segundo búfer tiene el tipo **SECBUFFER \_ EMPTY;** establezca los miembros **pvBuffer** y **cbBuffer** en cero.

</dd> <dt>

*Reserved2* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (Schannel),** este puntero recibe el nuevo identificador de contexto. En la segunda llamada, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

En las llamadas después de la primera llamada, pase el identificador devuelto aquí como parámetro *phContext* y especifique **NULL** para *phNewContext*.

</dd> <dt>

*pOutput* \[ in, out, optional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a la [**estructura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recibe los datos de salida. Si se ha especificado un búfer como SEC \_ READWRITE en la entrada, estará allí en la salida. El sistema asignará un búfer para el token de seguridad si se solicita (a través de ISC REQ ALLOCATE MEMORY) y rellenará la dirección en el descriptor del búfer para \_ \_ el token de \_ seguridad.

Si se especifica la marca ALLOCATE MEMORY de ISC \_ \_ REQ, el SSP de Schannel asignará memoria para el búfer y colocará la información adecuada en \_ [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc). Además, el autor de la llamada debe pasar un búfer de tipo **SECBUFFER \_ ALERT.** En la salida, si se genera una alerta, este búfer contiene información sobre esa alerta y se produce un error en la función.

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

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el paquete [*de seguridad devuelva*](../secgloss/s-gly.md) siempre este valor en la hora local. Este parámetro es opcional y se debe pasar **NULL** para clientes de corta duración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve uno de los siguientes códigos de éxito.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | El cliente debe llamar [**a CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y, a continuación, pasar la salida al servidor. A continuación, el cliente espera un token devuelto y lo pasa, en otra llamada, a [**InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md)<br/>                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | El cliente debe terminar de compilar el mensaje y, a continuación, llamar a [**la función CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | El cliente debe enviar el token de salida al servidor y esperar un token de devolución. A continuación, el token devuelto se pasa en otra llamada [**a InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) El token de salida puede estar vacío.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CREDENCIALES \_ \_ INCOMPLETAS DE SEC I \_**</dt> </dl> | El servidor ha solicitado la autenticación de cliente y las credenciales proporcionadas no incluyen un certificado o el certificado no lo emitió una entidad de certificación (CA) de confianza para el servidor. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                         |
| <dl> <dt>**MENSAJE \_ INCOMPLETO DE SEC E \_ \_**</dt> </dl>     | Los datos del mensaje completo no se leyeron de la conexión.<br/> Cuando se devuelve este valor, el búfer *pInput* contiene una estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **miembro BufferType** de **SECBUFFER \_ MISSING.** El **miembro cbBuffer** de **SecBuffer** contiene un valor que indica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se realiza correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento evitando varias llamadas a esta función.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | El [*contexto de seguridad*](../secgloss/s-gly.md) se inicializó correctamente. No es necesario realizar otra [**llamada a InitializeSecurityContext (Schannel).**](initializesecuritycontext--schannel.md) Si la función devuelve un token de salida, es decir, si secbuffer token en pOutput tiene una longitud distinta de cero, ese \_ token debe enviarse al servidor. <br/>                                                                                                                               |



 

Si se produce un error en la función, la función devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                            | Descripción                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>            | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERROR \_ INTERNO DE SEC E \_ \_**</dt> </dl>                 | Error que no se ha asignado a un código de error SSPI.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>                 | El identificador pasado a la función no es válido.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**TOKEN \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>                  | El error se debe a un token de entrada con formato incorrecto, como un token dañado en tránsito, un token de tamaño incorrecto o un token pasado a la delegación restringida [*incorrecta.*](../secgloss/s-gly.md) Puede pasar un token al paquete incorrecto si el cliente y el servidor no negociaron la delegación [*restringida adecuada.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**INICIO DE \_ SESIÓN DE SEC E \_ \_ DENEGADO**</dt> </dl>                   | Error de inicio de sesión.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl>   | No se pudo ponerse en contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría ser inaccesible o podría haber habido un error en la relación de confianza.<br/>                                                                                  |
| <dl> <dt>**S \_ E \_ SIN \_ CREDENCIALES**</dt> </dl>                 | No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).<br/>                                                                                                                                                  |
| <dl> <dt>**SEG \_ E \_ DESTINO \_ DESCONOCIDO**</dt> </dl>                 | No se ha reconocido el destino.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**SEC \_ E FUNCIÓN NO \_ \_ ADMITIDA**</dt> </dl>           | Se especificó una marca de atributo de contexto que no es válida (ISC REQ DELEGATE o \_ \_ ISC \_ REQ PROMPT FOR CREDS) en el \_ \_ parámetro \_ *fContextReq.*<br/>                                                                                                                                            |
| <dl> <dt>**SEC \_ E ENTIDAD DE SEGURIDAD \_ \_ INCORRECTA**</dt> </dl>                | La entidad de seguridad que recibió la solicitud de autenticación no es la misma que la que se pasó al *parámetro pszTargetName.* Esto indica un error en la autenticación mutua.<br/>                                                                                                          |
| <dl> <dt>**ERROR DE \_ COINCIDENCIA DEL PROTOCOLO DE APLICACIÓN \_ \_ \_ SEC E**</dt> </dl> | No existe ningún protocolo de aplicación común entre el cliente y el servidor.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó confidencialidad, pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente.

Si los atributos del contexto [*de seguridad*](../secgloss/s-gly.md) no son suficientes, el cliente debe liberar el contexto creado parcialmente llamando a la [**función DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

Un **cliente usa la función InitializeSecurityContext (Schannel)** para inicializar un contexto de salida.

Para un contexto de seguridad [*de dos etapas,*](../secgloss/s-gly.md)la secuencia de llamada es la siguiente:

1.  El cliente llama a la función con *phContext* establecido en **NULL** y rellena el descriptor del búfer con el mensaje de entrada.
2.  El [*paquete de seguridad*](../secgloss/s-gly.md) examina los parámetros y construye un token opaco, colocándolo en el elemento TOKEN de la matriz de búfer. Si el *parámetro fContextReq* incluye la marca ISC REQ ALLOCATE MEMORY, el paquete de seguridad asigna la memoria y devuelve el puntero en \_ el elemento \_ \_ TOKEN. [](../secgloss/s-gly.md)
3.  El cliente envía el token devuelto en el búfer *pOutput* al servidor de destino. A continuación, el servidor pasa el token como argumento de entrada en una llamada a la [**función AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md)
4.  [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) puede devolver un token, que el servidor envía al cliente para una segunda llamada a **InitializeSecurityContext (Schannel)** si la primera llamada devolvió SEC \_ I CONTINUE \_ \_ NEEDED.

Para los contextos de [*seguridad de*](../secgloss/s-gly.md)varias etapas, como la autenticación mutua, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función como se describió anteriormente, pero el paquete devuelve el código de éxito SEC \_ I \_ CONTINUE \_ NEEDED.
2.  El cliente envía el token de salida al servidor y espera la respuesta del servidor.
3.  Tras la recepción de la respuesta del servidor, el cliente llama de nuevo a **InitializeSecurityContext (Schannel),** con *phContext* establecido en el identificador que se devolvió de la última llamada. El token recibido del servidor se proporciona en el *parámetro pInput.*

Si el servidor ha respondido correctamente, el paquete [*de*](../secgloss/s-gly.md) seguridad devuelve SEC \_ E OK y se establece una sesión \_ segura.

Si la función devuelve una de las respuestas de error, no se acepta la respuesta del servidor y no se establece la sesión.

Si la función devuelve SEC I CONTINUE NEEDED, SEC I COMPLETE NEEDED o SEC I COMPLETE AND CONTINUE, se repiten los pasos \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 2 y 3.

Para inicializar [*un*](../secgloss/s-gly.md)contexto de seguridad, puede ser necesaria más de una llamada a esta función, en función del mecanismo de autenticación subyacente, así como de las opciones especificadas en el *parámetro fContextReq.*

Los *parámetros fContextReq* *y pfContextAttributes* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) El *parámetro pfContextAttributes* es válido en cualquier devolución correcta, pero solo en la devolución correcta final debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto. Los resultados intermedios pueden establecer, por ejemplo, la marca \_ ISC RET \_ ALLOCATED \_ MEMORY.

Si se establece la marca CREDS USE SUPPLIED DE ISC REQ, el paquete de seguridad debe buscar un tipo de búfer \_ \_ \_ \_ SECBUFFER PKG PARAMS [](../secgloss/s-gly.md) en el búfer de entrada \_ \_ *pInput.* No se trata de una solución genérica, pero permite un emparejamiento seguro de [*paquetes*](../secgloss/s-gly.md) de seguridad y aplicaciones cuando sea necesario.

Si se especificó ISC REQ ALLOCATE MEMORY, el autor de la llamada debe liberar la memoria mediante \_ una llamada a la función \_ \_ [**FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Por ejemplo, el token de entrada podría ser el desafío de un administrador de LAN. En este caso, el token de salida sería la respuesta cifrada con NTLM al desafío.

La acción que realiza el cliente depende del código de retorno de esta función. Si el código devuelto es SEC E OK, no habrá ninguna segunda llamada \_ \_ a **InitializeSecurityContext (Schannel)** y no se espera ninguna respuesta del servidor. Si el código devuelto es SEC I CONTINUE NEEDED, el cliente espera un token en respuesta del servidor y lo pasa en una segunda llamada \_ \_ a \_ **InitializeSecurityContext (Schannel).** El código de retorno SEC I COMPLETE NEEDED indica que el cliente debe terminar de compilar el mensaje y \_ llamar a la función \_ \_ [**CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) El código SEC \_ I COMPLETE AND CONTINUE incorpora ambas \_ \_ \_ acciones.

Si **InitializeSecurityContext (Schannel)** devuelve un resultado correcto en la primera (o solo) llamada, el autor de la llamada finalmente debe llamar a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) en el identificador devuelto, incluso si se produce un error en la llamada en una etapa posterior del intercambio de autenticación.

El cliente puede llamar a **InitializeSecurityContext (Schannel)** de nuevo después de que se haya completado correctamente. Esto indica al paquete [*de seguridad que*](../secgloss/s-gly.md) se quiere una reauauticación.

Los llamadores del modo kernel tienen las siguientes diferencias: el nombre de destino es una cadena [*Unicode*](../secgloss/u-gly.md) que se debe asignar en la memoria virtual mediante [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); no se debe asignar desde el grupo. Los búferes pasados y proporcionados *en pInput* y *pOutput* deben estar en la memoria virtual, no en el grupo.

Si la función devuelve SEC I INCOMPLETE CREDENTIALS, compruebe que especificó un certificado válido y \_ de confianza en sus \_ \_ credenciales. El certificado se especifica al llamar a la [**función AcquireCredentialsHandle (Schannel).**](acquirecredentialshandle--schannel.md) El certificado debe ser un certificado de autenticación de cliente emitido por una entidad de certificación (CA) de confianza para el servidor. Para obtener una lista de las CA de confianza para el servidor, llame a la función [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) y especifique el atributo SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.

Una vez que una aplicación cliente recibe un certificado de autenticación de una CA de confianza para el servidor, la aplicación crea una nueva credencial llamando a la función [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md) y, a continuación, llamando a **InitializeSecurityContext (Schannel)** de nuevo, especificando la nueva credencial en el *parámetro phCredential.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md)
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

 

 
