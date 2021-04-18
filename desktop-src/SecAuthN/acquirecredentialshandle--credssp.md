---
description: La función AcquireCredentialsHandle (CredSSP) adquiere un identificador a las credenciales preexistentes de una entidad de seguridad.
ms.assetid: 3b73decf-75d4-4bc4-b7ca-5f16aaadff29
title: Función AcquireCredentialsHandle (CredSSP)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 0dbece18bc7a7de8ec35764c9879380e29292e92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720558"
---
# <a name="acquirecredentialshandle-credssp-function"></a>Función AcquireCredentialsHandle (CredSSP)

La función **AcquireCredentialsHandle (CredSSP)** adquiere un identificador a las credenciales preexistentes de una entidad de seguridad. Este identificador es necesario para las funciones [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) y [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Pueden ser *credenciales* preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.

> [!Note]  
> No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.

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

Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.

> [!Note]  
> Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error. Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo contexto de seguridad se está ejecutando.

*pszPackage* \[ de\]

Puntero a una cadena terminada en null que especifica el nombre del paquete de seguridad con el que se utilizarán estas credenciales. Se trata de un nombre de paquete de seguridad devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/nf-sspi-enumeratesecuritypackagesa) . Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (CredSSP)**](querycontextattributes--credssp.md) con *UlAttribute* establecido en **SECPKG \_ ATTR \_ Package \_ info** para devolver información sobre el paquete de seguridad en uso.

*fCredentialUse* \[ de\]

Marca que indica cómo se utilizarán estas credenciales. Este parámetro puede ser uno de los valores siguientes.

| Valor                                                                                                                                                                                                                                        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SECPKG \_ de \_ entrada de cred**<br/>0x1  | Validar una credencial de servidor entrante. Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) o [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) . Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la **\_ \_ \_ \_ autoridad de autenticación**. La validación es específica del paquete |
| **SECPKG \_ CRED \_ saliente**<br/>0x0 | Permitir una credencial de cliente local para preparar un token saliente. |

*pvLogonId* \[ en, opcional\]

Un puntero a un [*identificador local único*](../secgloss/l-gly.md#_security_locally_unique_identifier_gly) (LUID) que identifica al usuario. Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red. Este parámetro puede ser **NULL**.

*pAuthData* \[ en, opcional\]

Puntero a una estructura [**\_ CRED de CREDSSP**](/windows/win32/api/credssp/ns-credssp-credssp_cred) que especifica los datos de autenticación para los paquetes Schannel y Negotiate.

*pGetKeyFn* \[ en, opcional\]

Reservado. Este parámetro no se utiliza y debe establecerse en **null**.

*pvGetKeyArgument* \[ en, opcional\]

Reservado. Este parámetro debe establecerse en **null**.

*phCredential* \[ enuncia\]

Un puntero a la estructura [CredHandle](sspi-handles.md) que recibirá el identificador de la credencial.

*ptsExpiry* \[ out, opcional\]

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas. El valor de estructura recibido depende del paquete de seguridad, que debe especificar el valor en la hora local.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **sec \_ E \_ OK**.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                      | Descripción                                                              |
|----------------------------------|--------------------------------------------------------------------------|
| **s \_ E \_ memoria insuficiente \_** | No hay suficiente memoria disponible para completar la acción solicitada. |
| **s \_ E \_ interno \_ error**      | Error que no se ha asignado a un código de error SSPI.                |
| **s \_ E \_ sin \_ credenciales**      | No hay credenciales disponibles en el paquete de seguridad.                    |
| **s \_ E \_ no \_ propietario**           | El autor de la llamada de la función no tiene las credenciales necesarias.      |
| **s \_ E \_ SECPKG \_ no \_ encontrados**   | El paquete de seguridad solicitado no existe.                           |
| **s \_ E \_ credenciales desconocidas \_** | No se reconocieron las credenciales proporcionadas al paquete.             |

## <a name="remarks"></a>Observaciones

La función **AcquireCredentialsHandle (CredSSP)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa un paquete de seguridad específico. La función puede devolver el identificador a las credenciales preexistentes o a las credenciales recién creadas y devolverlos. Este identificador se puede usar en las llamadas posteriores a las funciones [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md) y [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md) .

En general, **AcquireCredentialsHandle (CredSSP)** no proporciona las credenciales de otros usuarios que han iniciado sesión en el mismo equipo. Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/p-gly.md#_security_privilege_gly) de nombre TCB de se puede obtener las credenciales de una sesión de inicio de sesión existente especificando el [*identificador de inicio de sesión*](../secgloss/l-gly.md#_security_logon_identifier_gly) (LUID) de esa sesión. Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.

Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC. Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.

En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:

- Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) .
- Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.

Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows Vista \[\]                                              |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2008 \[\]                                        |
| Encabezado                   | SSPI. h (incluir Security. h)                                                      |
| Biblioteca                  | SECUR32. lib                                                                      |
| Archivo DLL                      | Secur32.dll                                                                      |
| Nombres Unicode y ANSI   | **AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI) |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (CredSSP)**](acceptsecuritycontext--credssp.md)
- [**InitializeSecurityContext (CredSSP)**](initializesecuritycontext--credssp.md)
- [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
