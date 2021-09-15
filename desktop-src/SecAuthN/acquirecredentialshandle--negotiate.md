---
description: Adquiere un identificador para las credenciales preexistentes de una entidad de seguridad que usa Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Función AcquireCredentialsHandle (Negotiate) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571920"
---
# <a name="acquirecredentialshandle-negotiate-function"></a>Función AcquireCredentialsHandle (Negotiate)

La **función AcquireCredentialsHandle (Negotiate)** adquiere un identificador para las credenciales preexistentes de una entidad [*de seguridad*](../secgloss/s-gly.md). Este identificador lo requieren las [**funciones InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) y [**AcceptSecurityContext (Negotiate).**](acceptsecuritycontext--negotiate.md) Pueden ser credenciales preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.

> [!Note]  
> No se trata de un "inicio de sesión en la red" y no implica la recopilación de credenciales.

 

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszPrincipal* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la entidad de seguridad a la que hará referencia el identificador.

> [!Note]  
> Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error. Una cadena null indica que el proceso requiere un identificador para las credenciales del usuario en cuyo contexto [*de seguridad*](../secgloss/s-gly.md) se está ejecutando.

 

</dd> <dt>

*pszPackage* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del paquete de [*seguridad*](../secgloss/s-gly.md) con el que se usarán estas credenciales. Se trata de [*un nombre de paquete*](../secgloss/s-gly.md) de seguridad devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la [**función EnumerateSecurityPackages.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) con *ulAttribute* establecido en SECPKG ATTR PACKAGE INFO para devolver información sobre el paquete de seguridad \_ en \_ \_ uso. [](../secgloss/s-gly.md)

Para llamar correctamente a esta función mediante Negotiate SSP, establezca este parámetro en "Negotiate".

</dd> <dt>

*fCredentialUse* \[ En\]
</dt> <dd>

Marca que indica cómo se usarán estas credenciales. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_ CRED \_ AUTOLOGON \_ RESTRICTED**</dt> <dt>0x00000010</dt> </dl> | La seguridad no usa credenciales de inicio de sesión predeterminadas ni credenciales [de Administrador de credenciales](credential-manager.md).<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ CRED \_ BOTH**</dt> </dl>                                                                                                                  | Valide una credencial entrante o use una credencial local para preparar un token saliente. Esta marca habilita las otras dos marcas.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ INBOUND**</dt> </dl>                                                                                                         | Valide una credencial de servidor entrante. Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) o [**AcceptSecurityContext (Negotiate).**](acceptsecuritycontext--negotiate.md) Si dicha autoridad no está disponible, la función producirá un error y devolverá SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY. La validación es específica del paquete.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ OUTBOUND**</dt> </dl>                                                                                                      | Permita que una credencial de cliente local prepare un token de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_ DIRECTIVA DE \_ \_ PROCESO CRED SOLO \_ 0x00000020**</dt> <dt></dt> </dl>   | La función procesa la directiva de servidor y devuelve **SEC \_ E NO \_ \_ CREDENTIALS**, lo que indica que la aplicación debe solicitar credenciales.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                             |



 

</dd> <dt>

*pvLogonID* \[ En\]
</dt> <dd>

Puntero a un [*identificador único local*](../secgloss/l-gly.md) (LUID) que identifica al usuario. Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red. Este parámetro puede ser **NULL**.

</dd> <dt>

*pAuthData* \[ En\]
</dt> <dd>

Puntero a datos específicos del paquete. Este parámetro puede ser **NULL,** lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete*](../secgloss/s-gly.md) de seguridad. Para usar las credenciales proporcionadas, pase una estructura **AUTH \_ IDENTITY \_ \_ \_ OPAQUE** de WINNT de PSEC devuelta por una llamada anterior a la función [**SspiPromptForCredentials.**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa)

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admiten el tipo **\_ \_ \_ \_ PSEC WINNT AUTH IDENTITY OPAQUE** y la función [**SspiPromptForCredentials.**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) Para usar las credenciales proporcionadas, pase un puntero a una estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) o [**SEC \_ WINNT \_ AUTH IDENTITY \_ \_ EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) que incluya esas credenciales.

El tiempo de ejecución de RPC pasa lo que se proporcionó [**en RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Cuando se usa el paquete Negotiate, las longitudes máximas de caracteres para el nombre de usuario, la contraseña y el dominio son 256, 256 y 15, respectivamente.

</dd> <dt>

*pGetKeyFn* \[ En\]
</dt> <dd>

Este parámetro no se usa y debe establecerse en **NULL.**

</dd> <dt>

*pvGetKeyArgument* \[ En\]
</dt> <dd>

Este parámetro no se usa y debe establecerse en **NULL.**

</dd> <dt>

*phCredential* \[ out\]
</dt> <dd>

Puntero a una [estructura CredHandle](sspi-handles.md) para recibir el identificador de credenciales.

</dd> <dt>

*ptsExpiry* \[ out\]
</dt> <dd>

Puntero a una [**estructura TimeStamp**](timestamp.md) que recibe la hora a la que expiran las credenciales devueltas. El valor devuelto en esta **estructura TimeStamp** depende de [*la delegación restringida*](../secgloss/s-gly.md). El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                 | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl> | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                  |
| <dl> <dt>**ERROR \_ INTERNO DE SEC E \_ \_**</dt> </dl>      | Error que no se ha asignado a un código de error SSPI.<br/>                                                                               |
| <dl> <dt>**S \_ E \_ SIN \_ CREDENCIALES**</dt> </dl>      | No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | El llamador de la función no tiene las credenciales necesarias.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG NO \_ \_ ENCONTRADO**</dt> </dl>   | El paquete [*de seguridad solicitado*](../secgloss/s-gly.md) no existe.<br/>                                                                                          |
| <dl> <dt>**CREDENCIALES \_ DESCONOCIDAS DE SEC E \_ \_**</dt> </dl> | No se han reconocido las credenciales proporcionadas al paquete.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

La **función AcquireCredentialsHandle (Negotiate)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o cliente, tal como lo usa una delegación [*restringida específica.*](../secgloss/s-gly.md) Puede ser el identificador de las credenciales preexistente o la función puede crear un nuevo conjunto de credenciales y devolverlo. Este identificador se puede usar en llamadas posteriores a las funciones [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) e [**InitializeSecurityContext (Negotiate).**](initializesecuritycontext--negotiate.md)

En general, **AcquireCredentialsHandle (Negotiate)** no permite que un proceso obtenga un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo. Sin embargo, un llamador con el privilegio SE TCB NAME tiene la opción de especificar el identificador de inicio de sesión \_ \_ (LUID) [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de esa sesión. Normalmente, esto lo usan los módulos en modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.

Un paquete podría llamar a la función *en pGetKeyFn* proporcionada por el transporte en tiempo de ejecución de RPC. Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **NULL.**

En el caso de los llamadores del modo kernel, se deben tener en cuenta las siguientes diferencias:

-   Los dos parámetros de cadena deben ser [*cadenas Unicode.*](../secgloss/u-gly.md)
-   Los valores de búfer deben asignarse en la memoria virtual del proceso, no desde el grupo.

Cuando haya terminado de usar las credenciales devueltas, libera la memoria usada por las credenciales mediante una llamada a la [**función FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
