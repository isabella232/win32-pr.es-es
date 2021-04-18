---
description: Permite al componente de servidor de una aplicación de transporte establecer un contexto de seguridad entre el servidor y un cliente remoto.
ms.assetid: a53f733e-b646-4431-b021-a2c446308849
title: AcceptSecurityContext (CredSSP) (función)
ms.topic: article
ms.date: 07/25/2019
ms.openlocfilehash: 681e03ea15729cc8726d63551e8b7b0a2b39ecac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720552"
---
# <a name="acceptsecuritycontext-credssp-function"></a>AcceptSecurityContext (CredSSP) (función)

La función **AcceptSecurityContext (CredSSP)** permite al componente de servidor de una aplicación de transporte establecer un contexto de seguridad entre el servidor y un cliente remoto. El cliente remoto llama a la función [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) para iniciar el proceso de establecer un contexto de seguridad. El servidor puede requerir uno o más tokens de respuesta del cliente remoto para completar el establecimiento del contexto de seguridad.

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

*phCredential* \[ en, opcional\]

Identificador de las credenciales del servidor. Para recuperar este identificador, el servidor llama a la función [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) con el valor de SECPKG \_ CRED \_ entrante o SECPKG \_ CRED \_ ambos establecidos.

*phContext* \[ en, opcional\]

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **AcceptSecurityContext (CredSSP)**, este puntero es **null**. En las llamadas posteriores, *phContext* especifica el contexto parcialmente formado que devuelve el parámetro *phNewContext* en la primera llamada.

*pInput* \[ en, opcional\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) generada por una llamada de cliente a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). La estructura contiene el descriptor de búfer de entrada.

El primer búfer debe ser del tipo **SECBUFFER \_ token** y contener el token de seguridad recibido del cliente. El segundo búfer debe ser de tipo **SECBUFFER \_ vacío**.

*fContextReq* \[ de\]

: Marcas de bits que especifican los atributos requeridos por el servidor para establecer el contexto. **Las marcas de bits** se pueden combinar mediante operaciones OR bit a bit. Este parámetro puede ser uno o varios de los valores siguientes.

| Value                          | Significado                                                                                                                                                                                                        |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ASC \_ req \_ asignar \_ memoria** | El proveedor de compatibilidad para seguridad de credenciales (CredSSP) asignará búferes de salida. Cuando haya terminado de usar los búferes de salida, liberelos mediante una llamada a la función [**FreeContextBuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) . |
| **\_conexión de REQ de ASC \_**       | El contexto de seguridad no controlará los mensajes de formato.                                                                                                                                                      |
| **\_delegado de REQ de ASC \_**         | El servidor puede suplantar al cliente. Omita esta marca para la delegación restringida.                                                         |
| **\_error de solicitud \_ EXTENDIda ASC \_**  | Cuando se produzcan errores, se notificará a la parte remota.                                                                                                                                                          |
| **\_detección de \_ repeticiones de ASC req \_**   | Detectar paquetes reproducidos.                                                                                                                                                                                       |
| **\_detección de \_ secuencia de REQ de ASC \_** | Detecta mensajes recibidos de la secuencia.                                                                                                                                                                      |
| **\_flujo de REQ de ASC \_**           | Admitir una conexión orientada a flujos.                                                                                                                                                                          |

Para ver posibles marcas de atributo y su significado, vea [requisitos de contexto](context-requirements.md). Las marcas usadas para este parámetro llevan el prefijo ASC \_ req, por ejemplo, \_ el \_ delegado de REQ.

Es posible que el cliente no admita los atributos solicitados. Para obtener más información, consulte el parámetro *pfContextAttr* .

*TargetDataRep* \[ de\]

Representación de los datos, como el orden de los bytes, en el destino. Este parámetro puede ser **\_ \_ DREP nativo de seguridad** o **\_ \_ DREP de seguridad de red**.

*phNewContext* \[ in, out, opcional\]

Puntero a una estructura [CtxtHandle](sspi-handles.md) . En la primera llamada a **AcceptSecurityContext (CredSSP)**, este puntero recibe el nuevo identificador de contexto. En las llamadas posteriores, *phNewContext* puede ser el mismo que el identificador especificado en el parámetro *phContext* .

*pOutput* \[ in, out, opcional\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) que contiene el descriptor del búfer de salida. Este búfer se envía al cliente para la entrada en llamadas adicionales a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md). Se puede generar un búfer de salida aunque la función devuelva SEC \_ E \_ Aceptar. Cualquier búfer generado debe volver a enviarse a la aplicación cliente.

En la salida, este búfer recibe un token para el contexto de seguridad. El token se debe enviar al cliente. La función también puede devolver un búfer de tipo SECBUFFER \_ extra.

*pfContextAttr* \[ enuncia\]

Un puntero a un conjunto de marcadores de bits que indica los atributos del contexto establecido. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md). Las marcas usadas para este parámetro tienen el prefijo ASC \_ RET, por ejemplo, el delegado de ASC \_ RET \_ .

No Compruebe los atributos relacionados con la seguridad hasta que la llamada a la función final se devuelva correctamente. Las marcas de atributo no relacionadas con la seguridad, como \_ la \_ marca ASC RET asignado \_ memoria, se pueden comprobar antes de la devolución final.

*ptsExpiry* \[ out, opcional\]

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora de expiración del contexto. Se recomienda que el paquete de seguridad devuelva siempre este valor en la hora local.

> [!Note]  
> Hasta la última llamada del proceso de autenticación, la hora de expiración del contexto puede ser incorrecta porque se proporcionará más información en las fases posteriores de la negociación. Por lo tanto, *ptsTimeStamp* debe ser **null** hasta la última llamada a la función.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve uno de los valores siguientes.

| Código o valor devuelto                                   | Descripción                                                                                                                                                                 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SEC_E_INCOMPLETE_MESSAGE <br/> 0x80090318L          | La función se ha realizado correctamente. Los datos del búfer de entrada están incompletos. La aplicación debe leer datos adicionales del cliente y llamar de nuevo a [<strong>AcceptSecurityContext (CredSSP)</strong>](acceptsecuritycontext--credssp.md) . |
| SEC_E_INSUFFICIENT_MEMORY <br/> 0x80090300L         | Error en la función. No hay suficiente memoria disponible para completar la acción solicitada.                                                                                 |
| SEC_E_INTERNAL_ERROR <br/> 0x80090304L              | Error en la función. Error que no se ha asignado a un código de error SSPI.                                                                                              |
| SEC_E_INVALID_HANDLE <br/> 0x80100003L              | Error en la función. El identificador pasado a la función no es válido.                                                                                                        |
| SEC_E_INVALID_TOKEN <br/> 0x80090308L               | Error en la función. El token que se ha pasado a la función no es válido.                                                                                                         |
| SEC_E_LOGON_DENIED <br/> 0x8009030CL                | Error de inicio de sesión.                                                                                                                                                           |
| SEC_E_NO_AUTHENTICATING_AUTHORITY <br/> 0x80090311L | Error en la función. No se pudo establecer contacto con ninguna autoridad para la autenticación. Esto puede deberse a las siguientes condiciones:<br/><ul><li>El nombre de dominio de la entidad de autenticación no es correcto.</li><li>El dominio no está disponible.</li><li>Error en la relación de confianza. |
| SEC_E_NO_CREDENTIALS <br/>0x8009030EL               | Error en la función. El identificador de credenciales especificado en el parámetro *phCredential* no es válido.                            |
| SEC_E_OK <br/> 0x00000000L                          | La función se ha realizado correctamente. Se aceptó el contexto de seguridad recibido del cliente. Si la función genera un token de salida, el token se debe enviar al proceso del cliente. |
| SEC_E_UNSUPPORTED_FUNCTION <br/> 0x80090302L        | Error en la función. El parámetro *fContextReq* especificó una marca de atributo de contexto (ASC_REQ_DELEGATE o ASC_REQ_PROMPT_FOR_CREDS) que no era válida.                       |
| SEC_I_COMPLETE_AND_CONTINUE <br/> 0x00090314L       | La función se ha realizado correctamente. El servidor debe llamar a [**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) y pasar el token de salida al cliente. Después, el servidor debe esperar un token de devolución del cliente antes de hacer otra llamada a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md). |
| SEC_I_COMPLETE_NEEDED <br/> 0x00090313L             | La función se ha realizado correctamente. El servidor debe terminar de compilar el mensaje desde el cliente antes de llamar a [ **CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)                             |
| SEC_I_CONTINUE_NEEDED <br/> 0x00090312L             | La función se ha realizado correctamente. El servidor debe enviar el token de salida al cliente y esperar un token devuelto. El token devuelto se debe pasar en *pInput* para otra llamada a [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md).


## <a name="remarks"></a>Observaciones

La función **AcceptSecurityContext (CredSSP)** es el homólogo del servidor para la función [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

Cuando el servidor recibe una solicitud de un cliente, usa el parámetro *fContextReq* para especificar lo que requiere la sesión. De este modo, un servidor puede requerir que los clientes sean capaces de usar una sesión confidencial o comprobada por [*integridad*](../secgloss/i-gly.md); puede rechazar clientes que no puedan satisfacer esa demanda. Como alternativa, un servidor no puede requerir nada; lo que el cliente necesita o puede proporcionar se devuelve en el parámetro *pfContextAttr* .

Los parámetros *fContextReq* y *pfContextAttr* son máscaras de texto que representan varios atributos de contexto. Para obtener una descripción de los distintos atributos, vea [requisitos de contexto](context-requirements.md).

> [!Note]  
> Aunque el parámetro *pfContextAttr* es válido en cualquier devolución correcta, debe examinar las marcas que pertenecen a los aspectos de seguridad del contexto solo en la devolución correcta final. Las devoluciones intermedias se pueden establecer, por ejemplo, la \_ \_ marca de memoria asignada de ISC \_ .

El autor de la llamada es responsable de determinar si los atributos de contexto finales son suficientes. Por ejemplo, si se solicitó la confidencialidad (cifrado) pero no se pudo establecer, algunas aplicaciones pueden optar por cerrar la conexión inmediatamente. Si no se puede establecer el contexto de seguridad, el servidor debe liberar el contexto creado parcialmente mediante una llamada a la función [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) . Para obtener información sobre cuándo se debe llamar a la función **DeleteSecurityContext** , vea **DeleteSecurityContext**.

Una vez establecido el contexto de seguridad, la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/win32/api/sspi/nf-sspi-querysecuritycontexttoken) para recuperar un identificador de la cuenta de usuario a la que se asignó el certificado de cliente. Además, el servidor puede usar la función [**ImpersonateSecurityContext**](/windows/win32/api/sspi/nf-sspi-impersonatesecuritycontext) para suplantar al usuario.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows Vista \[\]       |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2008 \[\] |
| Encabezado                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | SECUR32. lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**DeleteSecurityContext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
