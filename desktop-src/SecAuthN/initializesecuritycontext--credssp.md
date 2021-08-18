---
description: Inicia el contexto de seguridad de salida del lado cliente desde un identificador de credenciales.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: Función InitializeSecurityContext (CredSSP, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5ba38dd10552f90ecfcc5045b96edc5e62aff1f8a2beec0f2a728fc1f0be8c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015995"
---
# <a name="initializesecuritycontext-credssp-function"></a>Función InitializeSecurityContext (CredSSP)

La **función InitializeSecurityContext (CredSSP)** inicia el contexto de seguridad de salida del lado cliente desde un identificador de credenciales. La función crea un contexto de seguridad entre la aplicación cliente y un punto de conexión remoto. **InitializeSecurityContext (CredSSP)** devuelve un token que el cliente debe pasar al elemento remoto del mismo nivel. a su vez, el elemento del mismo nivel envía ese token a la implementación de seguridad local a través de [**la llamada AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Todos los llamadores deben considerar opaco el token generado.

Normalmente, se llama a **la función InitializeSecurityContext (CredSSP)** en un bucle hasta que se establece un contexto de seguridad suficiente.

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phCredential* \[ en, opcional\]
</dt> <dd>

Identificador de las credenciales [**devueltas por AcquireCredentialsHandle (CredSSP).**](acquirecredentialshandle--credssp.md) Este identificador se usa para generar el contexto de seguridad. La **función InitializeSecurityContext (CredSSP)** requiere al menos credenciales OUTBOUND.

</dd> <dt>

*phContext* \[ en, opcional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (CredSSP),** este puntero es **NULL.** En la segunda llamada, este parámetro es un puntero al identificador al contexto parcialmente formado devuelto en el *parámetro phNewContext* por la primera llamada.

En la primera llamada a **InitializeSecurityContext (CredSSP),** especifique **NULL.** En llamadas futuras, especifique el token recibido en el *parámetro phNewContext* después de la primera llamada a esta función.

</dd> <dt>

*pTargetName* \[ en, opcional\]
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

Marcas de bits que indican solicitudes para el contexto. No todos los paquetes pueden admitir todos los requisitos. Las marcas usadas para este parámetro tienen el prefijo ISC \_ REQ \_ , por ejemplo, ISC \_ REQ \_ DELEGATE.

Este parámetro puede ser uno o varios de los siguientes marcadores de atributos.



| Value                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ ALLOCATE \_ MEMORY**</dt> <dt>0x100</dt> </dl>                         | El paquete de seguridad asigna búferes de salida para el autor de la llamada. Cuando haya terminado de usar los búferes de salida, puede liberarlos llamando a la [**función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ ReQ \_ CONNECTION**</dt> <dt>0x800</dt> </dl>                                         | El contexto de seguridad no controlará los mensajes de formato.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ Error extendido \_ \_ de REQ**</dt> <dt>0x4000</dt> </dl>                           | Cuando se produzcan errores, se notificará a la parte remota.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ ReQ \_ MANUAL \_ CRED VALIDATION \_ 0x80000**</dt> <dt></dt> </dl> | El proveedor de compatibilidad con seguridad de credenciales (CredSSP) no debe autenticar el servidor automáticamente. Esta marca siempre se establece cuando se usa CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ ReQ \_ SEQUENCE \_ DETECT**</dt> <dt>0x8</dt> </dl>                           | Detectar los mensajes recibidos fuera de la secuencia.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ ReQ \_ STREAM**</dt> <dt>0x8000</dt> </dl>                                                    | Admite una conexión orientada a secuencias.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ REQ \_ USE \_ \_ CREDS**</dt> <dt>0X80</dt> </dl>                | CredSSP no debe intentar proporcionar credenciales para el cliente automáticamente.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ ReQ \_ DELEGATE**</dt> <dt>0x1</dt> </dl>                                                 | Indica que las credenciales del usuario se van a delegar en el servidor.<br/> Si no se especifica esta marca, se delega un conjunto vacío de credenciales al servidor.<br/> **Windows Server 2008 y Windows Vista:** Esta marca es obligatoria.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ Autenticación \_ mutua \_ de REQ**</dt> <dt>0x2</dt> </dl>                                       | Indica que no se requiere autenticación de servidor. Las directivas de delegación se siguen aplicando si no se especifica esta marca.<br/> **Windows Server 2008 y Windows Vista:** Esta marca se omite.<br/>                                                 |



 

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea el *parámetro pfContextAttr.*

Para obtener más descripciones de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

</dd> <dt>

*Reservado1* \[ En\]
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> <dt>

*TargetDataRep* \[ En\]
</dt> <dd>

Representación de datos, como la ordenación de bytes, en el destino. Este parámetro puede ser **SECURITY \_ NATIVE \_ DREP** o **SECURITY NETWORK \_ \_ DREP.**

</dd> <dt>

*pInput* \[ in, out, optional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a los búferes proporcionados como entrada al paquete. A menos que el servidor haya iniciado el contexto de cliente, el valor de este parámetro debe ser **NULL** en la primera llamada a la función. En las llamadas posteriores a la función o cuando el servidor inició el contexto de cliente, el valor de este parámetro es un puntero a un búfer asignado con memoria suficiente para contener el token devuelto por el equipo remoto.

En las llamadas a esta función después de la llamada inicial, debe haber dos búferes. El primero tiene el tipo **\_ SECBUFFER TOKEN** y contiene el token recibido del servidor. El segundo búfer tiene el tipo **SECBUFFER \_ EMPTY;** establezca los miembros **pvBuffer** y **cbBuffer** en cero.

</dd> <dt>

*Reservado2* \[ En\]
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> <dt>

*phNewContext* \[ in, out, optional\]
</dt> <dd>

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **InitializeSecurityContext (CredSSP),** este puntero recibe el nuevo identificador de contexto. En la segunda llamada, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

En las llamadas después de la primera llamada, pase el identificador devuelto aquí como parámetro *phContext* y especifique **NULL** para *phNewContext*.

</dd> <dt>

*pOutput* \[ out, opcional\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) A su vez, esta estructura contiene punteros a la [**estructura SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recibe los datos de salida. Si un búfer se escriba como **SEC \_ READWRITE** en la entrada, estará ahí en la salida. El sistema asignará un búfer para el token de seguridad si se solicita (a través de **ISC \_ REQ \_ ALLOCATE \_ MEMORY)** y rellenará la dirección en el descriptor del búfer para el token de seguridad.

Si se especifica la marca **\_ ISC REQ \_ ALLOCATE \_ MEMORY,** CredSSP asignará memoria para el búfer y colocará la información adecuada en [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ out\]
</dt> <dd>

Puntero a un conjunto de marcas de bits que indican los [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) del contexto establecido. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

Las marcas usadas para este parámetro tienen el prefijo ISC \_ RET, como **ISC \_ RET \_ DELEGATE.** Para obtener una lista de valores válidos, vea *el parámetro fContextReq.*

No compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo que no están relacionadas con la seguridad, como la marca **ASC \_ RET \_ ALLOCATED \_ MEMORY,** se pueden comprobar antes de la devolución final.

> [!Note]  
> Los atributos de contexto concretos pueden cambiar durante la negociación con un par remoto.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el paquete de seguridad devuelva siempre este valor en la hora local. Este parámetro es opcional y se debe pasar **NULL** para clientes de corta duración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve uno de los siguientes códigos de éxito.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MENSAJE \_ INCOMPLETO DE SEC E \_ \_**</dt> </dl>     | Los datos del mensaje completo no se leyeron de la conexión.<br/> Cuando se devuelve este valor, el búfer *pInput* contiene una estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un **miembro BufferType** de **SECBUFFER \_ MISSING**. El **miembro cbBuffer** de **SecBuffer** especifica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se realiza correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento evitando varias llamadas a esta función.<br/> |
| <dl> <dt>**SEC \_ E \_ OK**</dt> </dl>                      | El contexto de seguridad se inicializó correctamente. No es necesario realizar otra [**llamada a InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Si la función devuelve un token de salida (es decir, si **secbuffer \_ token** en *pOutput* es de longitud distinta de cero), ese token debe enviarse al servidor.<br/>                                                                                                   |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ AND \_ CONTINUE**</dt> </dl> | El cliente debe llamar [**a CompleteAuthToken y,**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) a continuación, pasar la salida al servidor. A continuación, el cliente espera un token devuelto y lo pasa, en otra llamada, a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**SEC \_ I \_ COMPLETE \_ NEEDED**</dt> </dl>        | El cliente debe terminar de compilar el mensaje y, a continuación, llamar a [**la función CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ I \_ CONTINUE \_ NEEDED**</dt> </dl>        | El cliente debe enviar el token de salida al servidor y esperar un token de devolución. El cliente pasa el token devuelto en otra llamada a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) El token de salida puede estar vacío.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**CREDENCIALES \_ \_ INCOMPLETAS DE SEC I \_**</dt> </dl> | El servidor ha solicitado la autenticación de cliente, pero las credenciales proporcionadas no incluyen un certificado o el certificado no lo emitió una entidad de certificación en la que confíe el servidor. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                              |



 

Si se produce un error en la función, la función devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                          | Descripción                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>          | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**ERROR \_ INTERNO DE SEC E \_ \_**</dt> </dl>               | Error que no se ha asignado a un código de error SSPI.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>               | El identificador pasado a la función no es válido.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**TOKEN \_ NO VÁLIDO DE SEC E \_ \_**</dt> </dl>                | El token de entrada tiene un formato de . Entre las posibles causas se incluyen un token dañado en tránsito, un token de tamaño incorrecto y un token pasado al paquete de seguridad incorrecto. Esta última condición puede producirse si el cliente y el servidor no negociaron el paquete de seguridad adecuado.<br/> |
| <dl> <dt>**INICIO DE \_ SESIÓN DE SEC E \_ \_ DENEGADO**</dt> </dl>                 | Error de inicio de sesión.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY**</dt> </dl> | No se pudo ponerse en contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría ser inaccesible o podría haber habido un error en la relación de confianza.<br/>                                                                    |
| <dl> <dt>**S \_ E \_ SIN \_ CREDENCIALES**</dt> </dl>               | No hay credenciales disponibles en el paquete de seguridad.<br/>                                                                                                                                    |
| <dl> <dt>**SEG \_ E \_ DESTINO \_ DESCONOCIDO**</dt> </dl>               | No se ha reconocido el destino.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E FUNCIÓN NO \_ \_ ADMITIDA**</dt> </dl>         | El valor del *parámetro fContextReq* no es válido. No se especificó una marca necesaria o se especificó una marca que no es compatible con CredSSP.<br/>                                                                                                                 |
| <dl> <dt>**SEC \_ E ENTIDAD DE SEGURIDAD \_ \_ INCORRECTA**</dt> </dl>              | La entidad de seguridad que recibió la solicitud de autenticación no es la misma que la que se pasó al *parámetro pszTargetName.* Este error indica un error en la autenticación mutua.<br/>                                                                                      |
| <dl> <dt>**SEC \_ E \_ DELEGATION \_ POLICY**</dt> </dl>            | La directiva no admite la delegación de credenciales en el servidor de destino.<br/>                                                                                                                                                                                                |
| <dl> <dt>**SEC \_ E \_ POLICY \_ NLTM \_ ONLY**</dt> </dl>            | No se permite la delegación de credenciales en el servidor de destino cuando no se logra la autenticación mutua.<br/>                                                                                                                                                                  |
| <dl> <dt>**ERROR \_ DE \_ AUTENTICACIÓN MUTUA \_ DE \_ SEC E**</dt> </dl>          | Error de autenticación del servidor cuando se especifica la marca AUTH mutual de ISC \_ REQ \_ en el parámetro \_ *fContextReq.*<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Comentarios

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó confidencialidad, pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente.

Si los atributos del contexto de seguridad no son suficientes, el cliente debe liberar el contexto creado parcialmente llamando a la [**función DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)

El cliente llama a **la función InitializeSecurityContext (CredSSP)** para inicializar un contexto de salida.

Para un contexto de seguridad de dos etapas, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función con *phContext* establecido en **NULL** y rellena el descriptor de búfer con el mensaje de entrada.
2.  El paquete de seguridad examina los parámetros y construye un token opaco, colocándolo en el elemento TOKEN de la matriz de búfer. Si el *parámetro fContextReq* incluye la marca **ISC \_ REQ \_ ALLOCATE \_ MEMORY,** el paquete de seguridad asigna la memoria y devuelve el puntero en el elemento TOKEN.
3.  El cliente envía el token devuelto en el búfer *pOutput* al servidor de destino. A continuación, el servidor pasa el token como argumento de entrada en una llamada a la [**función AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md)
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) puede devolver un token. El servidor envía este token al cliente a través de una segunda llamada a **InitializeSecurityContext (CredSSP)** si la primera llamada devolvió **SEC I CONTINUE \_ \_ \_ NEEDED**.

Si el servidor ha respondido correctamente, el paquete de seguridad devuelve **SEC \_ E \_ OK** y se establece una sesión segura.

Si la función devuelve una de las respuestas de error, no se acepta la respuesta del servidor y no se establece la sesión.

Si la función devuelve **SEC \_ I CONTINUE \_ \_ NEEDED**, **SEC I COMPLETE \_ \_ \_ NEEDED** o **SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE**, se repiten los pasos 2 y 3.

La inicialización del contexto de seguridad puede requerir más de una llamada a esta función, en función del mecanismo de autenticación subyacente, así como de las opciones especificadas en el *parámetro fContextReq.*

Los *parámetros fContextReq* *y pfContextAttributes* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) Aunque el *parámetro pfContextAttributes* es válido en cualquier devolución correcta, debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto solo en la devolución correcta final. Los resultados intermedios pueden establecer, por ejemplo, la marca **\_ ISC RET \_ ALLOCATED \_ MEMORY.**

Si la marca **USE \_ \_ \_ \_ SUPPLIED CREDS de ISC REQ** está establecida, el paquete de seguridad debe buscar un tipo de búfer **SECBUFFER \_ PKG \_ PARAMS** en el búfer de *entrada pInput.* Aunque esta no es una solución genérica, permite un emparejamiento seguro de paquete de seguridad y aplicación cuando sea necesario.

Si **se \_ especificó ISC REQ \_ ALLOCATE \_ MEMORY,** el autor de la llamada debe liberar la memoria mediante una llamada a [**la función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)

Por ejemplo, el token de entrada podría ser el desafío de un administrador de LAN. En este caso, el token de salida sería la respuesta cifrada con NTLM al desafío.

La acción que realiza el cliente depende del código de retorno de esta función. Si el código devuelto es **SEC \_ E \_ OK**, no habrá ninguna segunda llamada **a InitializeSecurityContext (CredSSP)** y no se espera ninguna respuesta del servidor. Si el código devuelto es **SEC \_ I CONTINUE \_ \_ NEEDED**, el cliente espera un token en respuesta del servidor y lo pasa en una segunda llamada a **InitializeSecurityContext (CredSSP).** El **código de retorno SEC I COMPLETE \_ \_ \_ NEEDED** indica que el cliente debe terminar de compilar el mensaje y llamar a [**la función CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) El **código SEC I COMPLETE AND \_ \_ \_ \_ CONTINUE** incorpora ambas acciones.

Si **InitializeSecurityContext (CredSSP)** devuelve un resultado correcto en la primera (o solo) llamada, el autor de la llamada finalmente debe llamar a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) en el identificador devuelto, incluso si se produce un error en la llamada en una etapa posterior del intercambio de autenticación.

El cliente puede volver a **llamar a InitializeSecurityContext (CredSSP)** después de que se haya completado correctamente. Esto indica al paquete de seguridad que se quiere una reauauticación.

Los llamadores en modo kernel tienen las siguientes diferencias: el nombre de destino es una cadena [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) que se debe asignar en la memoria virtual mediante [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); no se debe asignar desde el grupo. Los búferes pasados y proporcionados *en pInput* y *pOutput* deben estar en la memoria virtual, no en el grupo.

Si la función devuelve **SEC \_ I INCOMPLETE \_ \_ CREDENTIALS**, compruebe que las credenciales de r pasadas a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) especificaron un certificado válido y de confianza El certificado debe ser un certificado de autenticación de cliente emitido por una entidad de certificación de confianza para el servidor. Para obtener una lista de las CA de confianza para el servidor, llame a la función [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con el atributo **SECPKG \_ ATTR \_ ISSUER \_ LIST \_ EX.**

Después de recibir un certificado de autenticación de una entidad de certificación en la que confía el servidor, la aplicación cliente crea una nueva credencial. Para ello, llama a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) y, a continuación, vuelve a llamar a **InitializeSecurityContext (CredSSP),** especificando la nueva credencial en el *parámetro phCredential.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)
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

 

 
