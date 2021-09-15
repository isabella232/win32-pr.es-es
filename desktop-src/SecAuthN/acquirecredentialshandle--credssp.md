---
description: La función AcquireCredentialsHandle (CredSSP) adquiere un identificador para las credenciales preexistentes de una entidad de seguridad.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: Función AcquireCredentialsHandle (CredSSP)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571925"
---
# <a name="acquirecredentialshandle-credssp-function"></a>Función AcquireCredentialsHandle (CredSSP)

La **función AcquireCredentialsHandle (CredSSP)** adquiere un identificador para las credenciales preexistentes de una entidad de seguridad. Este identificador lo requieren las [**funciones InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) y [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Pueden ser credenciales preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.

> [!Note]  
> No se trata de un "inicio de sesión en la red" y no implica la recopilación de credenciales.

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_ENTRY AcquireCredentialsHandle(
  _In_opt_   SEC_CHAR       *pszPrincipal,
  _In_       SEC_CHAR       *pszPackage,
  _In_       unsigned long  fCredentialUse,
  _In_opt_   void           *pvLogonID,
  _In_opt_   void           *pAuthData,
  _In_opt_   SEC_GET_KEY_FN pGetKeyFn,
  _Reserved_ void           *pvGetKeyArgument,
  _Out_      PCredHandle    phCredential,
  _Out_opt_  PTimeStamp     ptsExpiry
);
```

## <a name="parameters"></a>Parámetros

*pszPrincipal* \[ en, opcional\]

Puntero a una cadena terminada en NULL que especifica el nombre de la entidad de seguridad a la que hará referencia el identificador.

> [!Note]  
> Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error. Una cadena null indica que el proceso requiere un identificador para las credenciales del usuario en cuyo contexto de seguridad se está ejecutando.

*pszPackage* \[ En\]

Puntero a una cadena terminada en NULL que especifica el nombre del paquete de seguridad con el que se usarán estas credenciales. Se trata de un nombre de paquete de seguridad devuelto en el **miembro Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la [**función EnumerateSecurityPackages.**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con *ulAttribute* establecido en **SECPKG \_ ATTR \_ PACKAGE \_ INFO** para devolver información sobre el paquete de seguridad en uso.

*fCredentialUse* \[ En\]

Marca que indica cómo se usarán estas credenciales. Este parámetro puede ser uno de los valores siguientes.

| Valor                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ CRED \_ INBOUND**<br/>0x1  | Valide una credencial de servidor entrante. Las credenciales entrantes se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) o [**AcceptSecurityContext (CredSSP).**](acceptsecuritycontext--credssp.md) Si dicha autoridad no está disponible, la función producirá un error y devolverá **SEC \_ E NO \_ \_ AUTHENTICATING \_ AUTHORITY**. La validación es específica del paquete |
| **SECPKG \_ CRED \_ OUTBOUND**<br/>0x0 | Permitir que una credencial de cliente local prepare un token de salida. |

*pvLogonId* \[ en, opcional\]

Puntero a un [*identificador único local*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) que identifica al usuario. Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red. Este parámetro puede ser **NULL**.

*pAuthData* \[ en, opcional\]

Puntero a una [**estructura \_ CRED de CRED de CRED DE CRED**](/windows/win32/api/credssp/ns-credssp-credssp_cred) que especifica los datos de autenticación para los paquetes Schannel y Negotiate.

*pGetKeyFn* \[ en, opcional\]

Reservado. Este parámetro no se usa y debe establecerse en **NULL.**

*pvGetKeyArgument* \[ en, opcional\]

Reservado. Este parámetro debe establecerse en **NULL.**

*phCredential* \[ out\]

Puntero a la [estructura CredHandle](sspi-handles.md) que recibirá el identificador de credenciales.

*ptsExpiry* \[ out, opcional\]

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora a la que expiran las credenciales devueltas. El valor de estructura recibido depende del paquete de seguridad, que debe especificar el valor en la hora local.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **SEC \_ E \_ OK**.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                      | Descripción                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **S \_ E \_ MEMORIA \_ INSUFICIENTE** | No hay memoria suficiente disponible para completar la acción solicitada. |
| **ERROR \_ INTERNO DE SEC E \_ \_**      | Error que no se ha asignado a un código de error SSPI.                |
| **S \_ E \_ SIN \_ CREDENCIALES**      | No hay credenciales disponibles en el paquete de seguridad.                    |
| **SEC \_ E \_ NOT \_ OWNER**           | El llamador de la función no tiene las credenciales necesarias.      |
| **SEC \_ E \_ SECPKG NO \_ \_ ENCONTRADO**   | El paquete de seguridad solicitado no existe.                           |
| **CREDENCIALES \_ DESCONOCIDAS DE SEC E \_ \_** | No se han reconocido las credenciales proporcionadas al paquete.             |

## <a name="remarks"></a>Observaciones

La **función AcquireCredentialsHandle (CredSSP)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o cliente, tal como lo usa un paquete de seguridad específico. La función puede devolver el identificador a las credenciales preexistente o a las credenciales recién creadas y devolverlo. Este identificador se puede usar en llamadas posteriores a las funciones [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) e [**InitializeSecurityContext (CredSSP).**](initializesecuritycontext--credssp.md)

En general, **AcquireCredentialsHandle (CredSSP)** no proporciona las credenciales de otros usuarios que iniciaron sesión en el mismo equipo. Sin embargo, un llamador con SE privilegio TCB NAME puede obtener las credenciales de una sesión de inicio de sesión existente especificando el identificador de inicio de sesión \_ \_ (LUID) de esa sesión. [](../secgloss/p-gly.md#_security_privilege_gly) [](../secgloss/l-gly.md#_security_logon_identifier_gly) Normalmente, esto lo usan los módulos en modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.

Un paquete podría llamar a la función *en pGetKeyFn* proporcionada por el transporte en tiempo de ejecución de RPC. Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **NULL.**

En el caso de los llamadores del modo kernel, se deben tener en cuenta las siguientes diferencias:

- Los dos parámetros de cadena deben ser [*cadenas Unicode.*](../secgloss/u-gly.md#_security_unicode_gly)
- Los valores de búfer deben asignarse en la memoria virtual del proceso, no desde el grupo.

Cuando haya terminado de usar las credenciales devueltas, libera la memoria usada por las credenciales mediante una llamada a la [**función FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio de Vista\]                                              |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2008 \[\]                                        |
| Encabezado                   | Sspi.h (incluir Security.h)                                                      |
| Biblioteca                  | Secur32.lib                                                                      |
| Archivo DLL                      | Secur32.dll                                                                      |
| Nombres Unicode y ANSI   | **AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Consulte también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
