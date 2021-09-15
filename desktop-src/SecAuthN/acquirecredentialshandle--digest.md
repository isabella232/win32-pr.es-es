---
description: Adquiere un identificador para las credenciales preexistentes de una entidad de seguridad que usa Digest.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: Función AcquireCredentialsHandle (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571921"
---
# <a name="acquirecredentialshandle-digest-function"></a>Función AcquireCredentialsHandle (Digest)

La **función AcquireCredentialsHandle (Digest)** adquiere un identificador para las credenciales preexistentes de una entidad [*de seguridad*](../secgloss/s-gly.md). Este identificador lo requieren las [**funciones AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md) Pueden ser credenciales preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.

> [!Note]  
> Esto no es un "inicio de sesión en la red" y no implica la recopilación de credenciales.

 

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

Puntero a una cadena terminada en NULL que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.

Cuando se usa el SSP de resumen, este parámetro es opcional.

> [!Note]  
> Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error. Una cadena null indica que el proceso requiere un identificador para las credenciales del usuario en cuyo contexto [*de seguridad*](../secgloss/s-gly.md) se está ejecutando.

 

</dd> <dt>

*pszPackage* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del paquete de [*seguridad*](../secgloss/s-gly.md) con el que se usarán estas credenciales. Se trata de [*un nombre de paquete*](../secgloss/s-gly.md) de seguridad devuelto en el miembro **Name** de una [**estructura SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la [**función EnumerateSecurityPackages.**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) con *ulAttribute* establecido en SECPKG ATTR PACKAGE INFO para devolver información sobre el paquete de seguridad \_ en \_ \_ uso. [](../secgloss/s-gly.md)

Cuando use el SSP de resumen, establezca este parámetro en WDIGEST \_ SP \_ NAME.

</dd> <dt>

*fCredentialUse* \[ En\]
</dt> <dd>

Marca que indica cómo se usarán estas credenciales. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ CRED \_ INBOUND**</dt> </dl>    | Valide una credencial de servidor entrante. Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) o [**AcceptSecurityContext (Digest).**](acceptsecuritycontext--digest.md) Si dicha entidad no está disponible, la función producirá un error y devolverá SEC \_ E \_ NO \_ AUTHENTICATING \_ AUTHORITY. La validación es específica del paquete.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ OUTBOUND**</dt> </dl> | Permitir que una credencial de cliente local prepare un token de salida.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*pvLogonID* \[ En\]
</dt> <dd>

Puntero a un [*identificador único local*](../secgloss/l-gly.md) (LUID) que identifica al usuario. Este parámetro se proporciona para los procesos del sistema de archivos, como los redireccionamientos de red. Este parámetro puede ser **NULL**.

</dd> <dt>

*pAuthData* \[ En\]
</dt> <dd>

Puntero a datos específicos del paquete. Este parámetro puede ser **NULL,** lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete*](../secgloss/s-gly.md) de seguridad. Para usar las credenciales proporcionadas, pase una estructura [**\_ SEC WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que incluya esas credenciales en este parámetro. El tiempo de ejecución de RPC pasa lo que se proporcionó [**en RpcBindingSetAuthInfo.**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)

Cuando se usa el SSP de resumen, este parámetro es un puntero a una estructura [**SEC \_ WINNT \_ AUTH \_ IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) que contiene información de autenticación que se va a usar para buscar las credenciales.

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

Este parámetro se establece en un tiempo máximo constante. No hay tiempo de expiración para las credenciales o contextos de seguridad [*de*](../secgloss/s-gly.md)resumen o cuando se usa el SSP de resumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                 | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl> | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                  |
| <dl> <dt>**ERROR \_ INTERNO DE SEC E \_ \_**</dt> </dl>      | Error que no se ha asignado a un código de error SSPI.<br/>                                                                               |
| <dl> <dt>**SEC \_ E \_ NO \_ CREDENTIALS**</dt> </dl>      | No hay credenciales disponibles en la [*delegación restringida.*](../secgloss/s-gly.md)<br/> |
| <dl> <dt>**SEC \_ E \_ NOT \_ OWNER**</dt> </dl>           | El llamador de la función no tiene las credenciales necesarias.<br/>                                                                     |
| <dl> <dt>**SEC \_ E \_ SECPKG \_ NOT \_ FOUND**</dt> </dl>   | El paquete [*de seguridad solicitado*](../secgloss/s-gly.md) no existe.<br/>                                                                                          |
| <dl> <dt>**CREDENCIALES DESCONOCIDAS DE SEC \_ E \_ \_**</dt> </dl> | No se han reconocido las credenciales proporcionadas al paquete.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

La **función AcquireCredentialsHandle (Digest)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal como lo usa una delegación [*restringida específica.*](../secgloss/s-gly.md) Puede ser el identificador de las credenciales preexistente o la función puede crear un nuevo conjunto de credenciales y devolverlo. Este identificador se puede usar en llamadas posteriores a las funciones [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) e [**InitializeSecurityContext (Digest).**](initializesecuritycontext--digest.md)

En general, **AcquireCredentialsHandle (Digest)** no permite que un proceso obtenga un identificador de las credenciales de otros usuarios que iniciaron sesión en el mismo equipo. Sin embargo, un autor de la llamada con SE privilegio TCB NAME tiene la opción de especificar el identificador de inicio de sesión \_ \_ (LUID) [](../secgloss/s-gly.md) [](../secgloss/l-gly.md) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de esa sesión. Normalmente, esto lo usan los módulos en modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.

Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte en tiempo de ejecución rpc. Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **NULL.**

En el caso de los llamadores de modo kernel, se deben tener en cuenta las siguientes diferencias:

-   Los dos parámetros de cadena deben ser [*cadenas Unicode.*](../secgloss/u-gly.md)
-   Los valores de búfer deben asignarse en la memoria virtual del proceso, no desde el grupo.

Cuando haya terminado de usar las credenciales devueltas, libera la memoria usada por las credenciales mediante una llamada a la [**función FreeCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
