---
description: Permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad entre el servidor y un cliente remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: Función AcceptSecurityContext (CredSSP)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568245"
---
# <a name="acceptsecuritycontext-credssp-function"></a>Función AcceptSecurityContext (CredSSP)

La **función AcceptSecurityContext (CredSSP)** permite que el componente de servidor de una aplicación de transporte establezca un contexto de seguridad entre el servidor y un cliente remoto. El cliente remoto llama a [**la función InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) para iniciar el proceso de establecimiento de un contexto de seguridad. El servidor puede requerir uno o varios tokens de respuesta del cliente remoto para completar el establecimiento del contexto de seguridad.

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_ENTRY AcceptSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    PSecBufferDesc pInput,
  _In_        unsigned long  fContextReq,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parámetros

*phCredential* \[ in, opcional\]

Identificador de las credenciales del servidor. Para recuperar este identificador, el servidor llama a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) con la marca SECPKG CRED INBOUND o \_ \_ SECPKG \_ CRED \_ BOTH establecida.

*phContext* \[ in, opcional\]

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (CredSSP),** este puntero es **NULL.** En las llamadas posteriores, *phContext* especifica el contexto parcialmente formado devuelto en el *parámetro phNewContext* por la primera llamada.

*pInput* \[ in, opcional\]

Puntero a una [**estructura SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generada por una llamada de cliente a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) La estructura contiene el descriptor del búfer de entrada.

El primer búfer debe ser de tipo **\_ SECBUFFER TOKEN** y contener el token de seguridad recibido del cliente. El segundo búfer debe ser de tipo **SECBUFFER \_ EMPTY.**

*fContextReq* \[ En\]

-Marcas de bits que especifican los atributos requeridos por el servidor para establecer el contexto. Las marcas de bits se pueden combinar mediante operaciones **OR** bit a bit. Este parámetro puede ser uno o varios de los valores siguientes.

| Value                          | Significado                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASIGNACIÓN DE MEMORIA DE ASC \_ REQ \_ \_** | El proveedor de compatibilidad de seguridad de credenciales (CredSSP) asignará búferes de salida. Cuando haya terminado de usar los búferes de salida, puede liberarlos llamando a la [**función FreeContextBuffer.**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) |
| **CONEXIÓN DE ASC \_ \_ REQ**       | El contexto de seguridad no controlará los mensajes de formato.                                                                                                                                                      |
| **ASC \_ REQ \_ DELEGATE**         | El servidor puede suplantar al cliente. Ignore esta marca para la delegación restringida.                                                         |
| **ERROR EXTENDIDO DE ASC \_ REQ \_ \_**  | Cuando se producen errores, se notificará a la parte remota.                                                                                                                                                          |
| **ASC \_ REQ \_ REPLAY \_ DETECT**   | Detectar paquetes reproducido.                                                                                                                                                                                       |
| **ASC \_ REQ \_ SEQUENCE \_ DETECT** | Detectar mensajes recibidos fuera de la secuencia.                                                                                                                                                                      |
| **SECUENCIA DE ASC \_ REQ \_**           | Admite una conexión orientada a secuencias.                                                                                                                                                                          |

Para ver las posibles marcas de atributo y sus significados, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen como prefijo ASC \_ REQ, por ejemplo, ASC \_ REQ \_ DELEGATE.

Es posible que el cliente no sea compatible con los atributos solicitados. Para obtener más información, vea *el parámetro pfContextAttr.*

*TargetDataRep* \[ En\]

Representación de datos, como la ordenación de bytes, en el destino. Este parámetro puede ser **SECURITY \_ NATIVE \_ DREP** o **SECURITY NETWORK \_ \_ DREP.**

*phNewContext* \[ in, out, optional\]

Puntero a una [estructura CtxtHandle.](sspi-handles.md) En la primera llamada a **AcceptSecurityContext (CredSSP),** este puntero recibe el nuevo identificador de contexto. En las llamadas posteriores, *phNewContext* puede ser el mismo que el identificador especificado en el *parámetro phContext.*

*pOutput* \[ in, out, optional\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene el descriptor del búfer de salida. Este búfer se envía al cliente para su entrada en llamadas adicionales a [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md) Se puede generar un búfer de salida incluso si la función devuelve SEC \_ E \_ OK. Cualquier búfer generado debe devolverse a la aplicación cliente.

En la salida, este búfer recibe un token para el contexto de seguridad. El token debe enviarse al cliente. La función también puede devolver un búfer de tipo SECBUFFER \_ EXTRA.

*pfContextAttr* \[ out\]

Puntero a un conjunto de marcas de bits que indican los atributos del contexto establecido. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md) Las marcas usadas para este parámetro tienen el prefijo ASC \_ RET, por ejemplo, ASC \_ RET \_ DELEGATE.

No compruebe los atributos relacionados con la seguridad hasta que la llamada de función final se devuelva correctamente. Las marcas de atributo no relacionadas con la seguridad, como la marca ASC RET ALLOCATED MEMORY, se pueden comprobar \_ \_ antes de la \_ devolución final.

*ptsExpiry* \[ out, opcional\]

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora de expiración del contexto. Se recomienda que el paquete de seguridad devuelva siempre este valor en la hora local.

> [!Note]  
> Hasta la última llamada del proceso de autenticación, la hora de expiración del contexto puede ser incorrecta porque se proporciona más información durante las fases posteriores de la negociación. Por lo tanto, *ptsTimeStamp* debe ser **NULL hasta** la última llamada a la función.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.

| Código o valor devuelto                                   | Descripción                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | La función se ha realizado correctamente. Los datos del búfer de entrada están incompletos. La aplicación debe leer datos adicionales del cliente y llamar de nuevo [<strong>a AcceptSecurityContext (CredSSP).</strong>](acceptsecuritycontext--credssp.md) |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | Error en la función. No hay suficiente memoria disponible para completar la acción solicitada.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | Error en la función. Error que no se ha asignado a un código de error SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | Error en la función. El identificador pasado a la función no es válido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | Error en la función. El token pasado a la función no es válido.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Error de inicio de sesión.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | Error en la función. No se pudo ponerse en contacto con ninguna autoridad para la autenticación. Esto podría deberse a las siguientes condiciones:<br/><ul><li>El nombre de dominio de la entidad de autenticación es incorrecto.</li><li>El dominio no está disponible.</li><li>Error en la relación de confianza. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | Error en la función. El identificador de credenciales especificado en el *parámetro phCredential* no es válido.                            |
| SEC_E_OK <br/> 0x00000000L                          | La función se ha realizado correctamente. Se aceptó el contexto de seguridad recibido del cliente. Si la función generó un token de salida, el token debe enviarse al proceso de cliente. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | Error en la función. El *parámetro fContextReq* especificó una marca de atributo de contexto (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) que no era válida.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | La función se ha realizado correctamente. El servidor debe llamar [**a CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y pasar el token de salida al cliente. A continuación, el servidor debe esperar un token de devolución del cliente antes de realizar otra llamada a [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | La función se ha realizado correctamente. El servidor debe terminar de compilar el mensaje del cliente antes de llamar a [ **CompleteAuthToken.**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | La función se ha realizado correctamente. El servidor debe enviar el token de salida al cliente y esperar un token devuelto. El token devuelto debe pasarse en *pInput para* otra llamada a [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md)


## <a name="remarks"></a>Observaciones

La **función AcceptSecurityContext (CredSSP)** es el homólogo del servidor de la [**función InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)

Cuando el servidor recibe una solicitud de un cliente, usa el parámetro *fContextReq* para especificar lo que requiere de la sesión. De este modo, un servidor puede requerir que los clientes puedan usar una sesión confidencial o [*comprobada*](../secgloss/i-gly.md)por integridad. puede rechazar clientes que no pueden satisfacer esa demanda. Como alternativa, un servidor no puede requerir nada; todo lo que el cliente requiere o puede proporcionar se devuelve en el *parámetro pfContextAttr.*

Los *parámetros fContextReq* *y pfContextAttr* son máscaras de bits que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [Requisitos de contexto.](context-requirements.md)

> [!Note]  
> Aunque el *parámetro pfContextAttr es* válido en cualquier devolución correcta, debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto solo en la devolución correcta final. Los resultados intermedios pueden establecer, por ejemplo, la marca \_ ISC RET \_ ALLOCATED \_ MEMORY.

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Por ejemplo, si se solicitó la confidencialidad (cifrado) pero no se pudo establecer, algunas aplicaciones pueden optar por apagar la conexión inmediatamente. Si no se puede establecer el contexto de seguridad, el servidor debe liberar el contexto creado parcialmente llamando a la [**función DeleteSecurityContext.**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) Para obtener información sobre cuándo llamar a **la función DeleteSecurityContext,** **vea DeleteSecurityContext**.

Una vez establecido el contexto de seguridad, la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar un identificador de la cuenta de usuario a la que se asignó el certificado de cliente. Además, el servidor puede usar la [**función ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar al usuario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows aplicaciones de escritorio de Vista \[\]       |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2008 \[\] |
| Encabezado                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Consulte también

- [Funciones de SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
