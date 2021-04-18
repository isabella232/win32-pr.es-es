---
description: Inicia el lado cliente, el contexto de seguridad de salida de un identificador de credencial.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: Función InitializeSecurityContext (CredSSP, Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: aa359fc0cedf96f43d93cfb7d962035453328759
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720321"
---
# <a name="initializesecuritycontext-credssp-function"></a>InitializeSecurityContext (CredSSP) (función)

La función **InitializeSecurityContext (CredSSP)** inicia el contexto de seguridad de salida del lado cliente desde un identificador de credencial. La función crea un contexto de seguridad entre la aplicación cliente y un elemento remoto del mismo nivel. **InitializeSecurityContext (CredSSP)** devuelve un token que el cliente debe pasar al elemento remoto del mismo nivel; a su vez, el elemento del mismo nivel envía ese token a la implementación de seguridad local a través de la llamada a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . El token generado debe considerarse opaco por todos los llamadores.

Normalmente, se llama a la función **InitializeSecurityContext (CredSSP)** en un bucle hasta que se establece un contexto de seguridad suficiente.

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

Identificador de las credenciales devueltas por [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md). Este identificador se utiliza para compilar el contexto de seguridad. La función **InitializeSecurityContext (CredSSP)** requiere al menos credenciales de salida.

</dd> <dt>

*phContext* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **InitializeSecurityContext (CredSSP)**, este puntero es **null**. En la segunda llamada, este parámetro es un puntero al identificador para el contexto parcialmente formado devuelto en el parámetro *phNewContext* por la primera llamada a.

En la primera llamada a **InitializeSecurityContext (CredSSP)**, especifique **null**. En futuras llamadas, especifique el token recibido en el parámetro *phNewContext* después de la primera llamada a esta función.

</dd> <dt>

*pTargetName* \[ en, opcional\]
</dt> <dd>

Un puntero a una cadena terminada en null que identifica de forma única el servidor de destino. Schannel usa este valor para comprobar el certificado del servidor. Schannel también usa este valor para buscar la sesión en la memoria caché de la sesión al volver a establecer una conexión. La sesión almacenada en caché solo se utiliza si se cumplen todas las condiciones siguientes:

-   El nombre de destino es el mismo.
-   La entrada de caché no ha expirado.
-   El proceso de aplicación que llama a la función es el mismo.
-   La sesión de inicio de sesión es la misma.
-   El identificador de la credencial es el mismo.

</dd> <dt>

*fContextReq* \[ de\]
</dt> <dd>

Marcas de bits que indican las solicitudes para el contexto. No todos los paquetes pueden admitir todos los requisitos. Las marcas usadas para este parámetro llevan el prefijo de ISC \_ req \_ , por ejemplo, el delegado de REQ de ISC \_ \_ .

Este parámetro puede ser uno o varios de los siguientes marcadores de atributos.



| Value                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ REQ \_ asignar \_ memoria**</dt> <dt>0x100</dt> </dl>                         | El paquete de seguridad asigna búferes de salida para el autor de la llamada. Cuando haya terminado de usar los búferes de salida, liberelos mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ \_Conexión de REQ**</dt> , <dt>0x800</dt> </dl>                                         | El contexto de seguridad no controlará los mensajes de formato.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ 0x4000 \_ de \_ error extendido de REQ**</dt> <dt></dt> </dl>                           | Cuando se produzcan errores, se notificará a la parte remota.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ \_ \_ \_ Validación de credenciales manuales de REQ**</dt> <dt>0x80000</dt> </dl> | El proveedor de compatibilidad para seguridad de credenciales (CredSSP) no debe autenticar el servidor automáticamente. Esta marca siempre se establece cuando se usa CredSSP.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ Secuencia de REQ \_ \_ detectar**</dt> <dt>0x8</dt> </dl>                           | Detecta mensajes recibidos de la secuencia.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ \_Secuencia req**</dt> <dt>0x8000</dt> </dl>                                                    | Admitir una conexión orientada a flujos.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ \_Uso de \_ \_ credenciales proporcionadas**</dt> por el uso de REQ <dt></dt> </dl>                | CredSSP no debe intentar proporcionar credenciales para el cliente automáticamente.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ \_Delegado de REQ**</dt> <dt>0x1</dt> </dl>                                                 | Indica que las credenciales del usuario se van a delegar en el servidor.<br/> Si no se especifica esta marca, se delega un conjunto vacío de credenciales al servidor.<br/> **Windows Server 2008 y Windows Vista:** Esta marca es obligatoria.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ SOLICITUD \_ mutua de \_ autenticación**</dt> <dt>0X2</dt> </dl>                                       | Indica que no se requiere autenticación del servidor. Las directivas de delegación se siguen aplicando si no se especifica esta marca.<br/> **Windows Server 2008 y Windows Vista:** Esta marca se omite.<br/>                                                 |



 

Es posible que el cliente no admita los atributos solicitados. Para obtener más información, consulte el parámetro *pfContextAttr* .

Para obtener más descripciones de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

</dd> <dt>

*Reserved1* \[ de\]
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> <dt>

*TargetDataRep* \[ de\]
</dt> <dd>

Representación de los datos, como el orden de los bytes, en el destino. Este parámetro puede ser **\_ \_ DREP nativo de seguridad** o **\_ \_ DREP de seguridad de red**.

</dd> <dt>

*pInput* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene punteros a los búferes proporcionados como entrada para el paquete. A menos que el servidor inicie el contexto del cliente, el valor de este parámetro debe ser **null** en la primera llamada a la función. En las llamadas subsiguientes a la función o cuando el servidor inició el contexto de cliente, el valor de este parámetro es un puntero a un búfer asignado con suficiente memoria para contener el token devuelto por el equipo remoto.

En las llamadas a esta función después de la llamada inicial, debe haber dos búferes. El primero tiene el tipo **SECBUFFER \_ token** y contiene el token recibido del servidor. El segundo búfer tiene el tipo **SECBUFFER \_ vacío**; establezca los miembros **pvBuffer** y **cbBuffer** en cero.

</dd> <dt>

*Reserved2* \[ de\]
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> <dt>

*phNewContext* \[ in, out, opcional\]
</dt> <dd>

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **InitializeSecurityContext (CredSSP)**, este puntero recibe el nuevo identificador de contexto. En la segunda llamada, *phNewContext* puede ser el mismo que el identificador especificado en el parámetro *phContext* .

En las llamadas después de la primera llamada, pase el identificador que se devuelve aquí como parámetro *phContext* y especifique **null** para *phNewContext*.

</dd> <dt>

*pOutput* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . A su vez, esta estructura contiene punteros a la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que recibe los datos de salida. Si se ha escrito un búfer como lectura en segundo/lectura en la entrada, se mostrará en la salida. **\_** El sistema asignará un búfer para el token de seguridad si se solicita (a través de la **\_ solicitud de asignación de \_ \_ memoria de ISC**) y rellenará la dirección en el descriptor de búfer para el token de seguridad.

Si se especifica la marca **ISC \_ req \_ allocate \_ Memory** , CredSSP asignará memoria para el búfer y colocará la información adecuada en [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc).

</dd> <dt>

*pfContextAttr* \[ enuncia\]
</dt> <dd>

Un puntero a un conjunto de marcadores de bits que indica los [*atributos*](../secgloss/a-gly.md#_security_attribute_gly) del contexto establecido. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

Las marcas usadas para este parámetro llevan el prefijo ISC \_ RET, como **el \_ \_ delegado de ISC RET**. Para obtener una lista de valores válidos, vea el parámetro *fContextReq* .

No Compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo que no están relacionadas con la seguridad, como la marca ASC RET allocated **\_ \_ \_ Memory** , se pueden comprobar antes de la devolución final.

> [!Note]  
> Los atributos de contexto concretos pueden cambiar durante la negociación con un elemento remoto del mismo nivel.

 

</dd> <dt>

*ptsExpiry* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora de expiración del contexto. Se recomienda que el paquete de seguridad devuelva siempre este valor en la hora local. Este parámetro es opcional y se debe pasar **null** para los clientes de corta duración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve uno de los siguientes códigos de éxito.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ mensaje incompleto \_**</dt> </dl>     | Los datos de todo el mensaje no se leyeron desde la conexión.<br/> Cuando se devuelve este valor, el búfer *pInput* contiene una estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) con un miembro **BufferType** de **SecBuffer \_ que falta**. El miembro **cbBuffer** de **SecBuffer** especifica el número de bytes adicionales que la función debe leer del cliente antes de que esta función se ejecute correctamente. Aunque este número no siempre es preciso, su uso puede ayudar a mejorar el rendimiento al evitar varias llamadas a esta función.<br/> |
| <dl> <dt>**s \_ E \_ Aceptar**</dt> </dl>                      | El contexto de seguridad se inicializó correctamente. No es necesario otra llamada [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) . Si la función devuelve un token de salida, es decir, si el **\_ token de SECBUFFER** en *pOutput* tiene una longitud distinto de cero, ese token se debe enviar al servidor.<br/>                                                                                                   |
| <dl> <dt>**s \_ \_ finalización \_ y \_ continuación**</dt> </dl> | El cliente debe llamar a [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y, a continuación, pasar la salida al servidor. Después, el cliente espera un token devuelto y lo pasa, en otra llamada, a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md).<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ \_ finalización \_ necesaria**</dt> </dl>        | El cliente debe terminar de compilar el mensaje y, a continuación, llamar a la función [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ \_ \_**</dt> </dl>        | El cliente debe enviar el token de salida al servidor y esperar a que se devuelva un token. El cliente pasa el token devuelto en otra llamada a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). El token de salida puede estar vacío.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**s \_ I \_ credenciales incompletas \_**</dt> </dl> | El servidor solicitó la autenticación del cliente, pero las credenciales proporcionadas no incluyen un certificado, o bien una entidad de certificación en la que confía el servidor no emitió el certificado. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                              |



 

Si se produce un error en la función, la función devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                          | Descripción                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memoria insuficiente \_**</dt> </dl>          | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ interno \_ error**</dt> </dl>               | Error que no se ha asignado a un código de error SSPI.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ identificador no válido \_**</dt> </dl>               | El identificador pasado a la función no es válido.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ E \_ token no válido \_**</dt> </dl>                | El token de entrada tiene un formato incorrecto. Entre las posibles causas se incluyen un token dañado en tránsito, un token de tamaño incorrecto y un token pasado al paquete de seguridad equivocado. Esta última condición puede producirse si el cliente y el servidor no negociaron el paquete de seguridad adecuado.<br/> |
| <dl> <dt>**s \_ E \_ Inicio de sesión \_ denegado**</dt> </dl>                 | Error de inicio de sesión.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ sin \_ entidad de autenticación \_**</dt> </dl> | No se pudo establecer contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría estar inaccesible o podría haber un error de relación de confianza.<br/>                                                                    |
| <dl> <dt>**s \_ E \_ sin \_ credenciales**</dt> </dl>               | No hay credenciales disponibles en el paquete de seguridad.<br/>                                                                                                                                    |
| <dl> <dt>**s \_ E \_ destino \_ desconocido**</dt> </dl>               | No se reconoció el destino.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ función no admitida \_**</dt> </dl>         | El valor del parámetro *fContextReq* no es válido. No se especificó una marca requerida o se especificó una marca que no es compatible con CredSSP.<br/>                                                                                                                 |
| <dl> <dt>**s \_ E \_ entidad de seguridad equivocada \_**</dt> </dl>              | La entidad de seguridad que recibió la solicitud de autenticación no es la misma que la que se pasa al parámetro *pszTargetName* . Este error indica un error en la autenticación mutua.<br/>                                                                                      |
| <dl> <dt>**\_Directiva de \_ delegación s E sec \_**</dt> </dl>            | La Directiva no admite la delegación de credenciales en el servidor de destino.<br/>                                                                                                                                                                                                |
| <dl> <dt>**s \_ & \_ NLTM de directiva de \_ seg. \_**</dt> </dl>            | No se permite la delegación de credenciales en el servidor de destino cuando no se logra la autenticación mutua.<br/>                                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ Mutual \_ auth \_**</dt> </dl>          | No se pudo autenticar el servidor cuando \_ \_ \_ se especifica la marca de autenticación mutua req de ISC en el parámetro *fContextReq* .<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Observaciones

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Si, por ejemplo, se solicitó la confidencialidad, pero no se pudo establecer, algunas aplicaciones pueden optar por cerrar la conexión inmediatamente.

Si los atributos del contexto de seguridad no son suficientes, el cliente debe liberar el contexto creado parcialmente mediante una llamada a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) .

El cliente llama a la función **InitializeSecurityContext (CredSSP)** para inicializar un contexto de salida.

Para un contexto de seguridad de dos tramos, la secuencia de llamada es la siguiente:

1.  El cliente llama a la función con *phContext* establecido en **null** y rellena el descriptor del búfer con el mensaje de entrada.
2.  El paquete de seguridad examina los parámetros y construye un token opaco, colocándolo en el elemento de TOKEN en la matriz de búferes. Si el parámetro *fContextReq* incluye la marca **ISC \_ req \_ allocate \_ Memory** , el paquete de seguridad asigna la memoria y devuelve el puntero en el elemento token.
3.  El cliente envía el token devuelto en el búfer de *pOutput* al servidor de destino. A continuación, el servidor pasa el token como argumento de entrada en una llamada a la función [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) .
4.  [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) puede devolver un token. El servidor envía este token al cliente a través de una segunda llamada a **InitializeSecurityContext (CredSSP)** si la primera llamada que se devuelve es el segundo que **\_ se \_ \_ necesita**.

Si el servidor ha respondido correctamente, el paquete de seguridad devuelve **sec \_ e \_ OK** y se establece una sesión segura.

Si la función devuelve una de las respuestas de error, no se acepta la respuesta del servidor y no se establece la sesión.

Si la función devuelve los **segundos que \_ se \_ \_ necesitan para continuar**, **\_ \_ \_ es necesario que se complete** la segunda vez o se repiten los pasos 2 y 3. **\_ \_ \_ \_**

La inicialización del contexto de seguridad puede requerir más de una llamada a esta función, dependiendo del mecanismo de autenticación subyacente, así como de las opciones especificadas en el parámetro *fContextReq* .

Los parámetros *fContextReq* y *pfContextAttributes* son máscaras de texto que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md). Aunque el parámetro *pfContextAttributes* es válido en cualquier devolución correcta, debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto solo en la devolución correcta final. Las devoluciones intermedias se pueden establecer, por ejemplo, la marca de **\_ \_ \_ memoria asignada de ISC** .

Si se establece la marca de **\_ \_ \_ \_ credenciales proporcionadas** por el uso de ISC, el paquete de seguridad debe buscar un tipo de búfer **\_ \_ params de SECBUFFER pkg** en el búfer de entrada *pInput* . Aunque esta no es una solución genérica, permite un fuerte emparejamiento del paquete de seguridad y de la aplicación cuando sea necesario.

Si se especificó la **\_ solicitud de asignación de \_ \_ memoria de ISC** , el llamador debe liberar la memoria mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) .

Por ejemplo, el token de entrada podría ser el desafío de un administrador de LAN. En este caso, el token de salida sería la respuesta cifrada NTLM al desafío.

La acción que realiza el cliente depende del código de retorno de esta función. Si el código de retorno es en **segundos \_ E \_ OK**, no habrá ninguna segunda llamada a **InitializeSecurityContext (CredSSP)** y no se espera ninguna respuesta del servidor. Si el código de retorno es la **\_ \_ \_ necesidad de continuar**, el cliente espera un token en respuesta del servidor y lo pasa en una segunda llamada a **InitializeSecurityContext (CredSSP)**. El código de retorno **seg. de \_ \_ finalización \_ necesario** indica que el cliente debe terminar de compilar el mensaje y llamar a la función [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) . El código **sec \_ I \_ Complete \_ y \_ continue** incorpora ambas acciones.

Si **InitializeSecurityContext (CredSSP)** devuelve SUCCESS en la primera llamada (o solo), el llamador debe llamar finalmente a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) en el identificador devuelto, incluso si se produce un error en la llamada en un segmento posterior del intercambio de autenticación.

El cliente puede llamar a **InitializeSecurityContext (CredSSP)** una vez que se ha completado correctamente. Esto indica al paquete de seguridad que se desea una reautenticación.

Los llamadores de modo kernel tienen las siguientes diferencias: el nombre de destino es una cadena [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) que debe asignarse en la memoria virtual mediante [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc); no debe estar asignado desde el grupo. Los búferes pasados y proporcionados en *pInput* y *pOutput* deben estar en la memoria virtual, no en el grupo.

Si la función devuelve **\_ \_ \_ las credenciales s incompletas**, compruebe que las credenciales de r que se pasan a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) especifican un certificado válido y de confianza. el certificado debe ser un certificado de autenticación de cliente emitido por una entidad de certificación que sea de confianza para el servidor. Para obtener una lista de las entidades de certificación de confianza del servidor, llame a la función [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con el atributo de **\_ \_ \_ lista \_ de emisores de SECPKG ATTR** .

Después de recibir un certificado de autenticación de una entidad de certificación en la que el servidor confía, la aplicación cliente crea una nueva credencial. Para ello, llama a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) y, después, llama a **InitializeSecurityContext (CredSSP)** de nuevo, especificando la nueva credencial en el parámetro *phCredential* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
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

 

 
