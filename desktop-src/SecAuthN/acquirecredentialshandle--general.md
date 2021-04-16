---
description: Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: AcquireCredentialsHandle (general) (función) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720663"
---
# <a name="acquirecredentialshandle-general-function"></a>AcquireCredentialsHandle (general), función

La función **AcquireCredentialsHandle (general)** adquiere un identificador a las credenciales preexistentes de una [*entidad de seguridad*](../secgloss/s-gly.md). Este identificador es necesario para las funciones [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) y [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) . Pueden ser credenciales preexistentes, que se establecen a través de un inicio de sesión del sistema que no se describe aquí, o bien el autor de la llamada puede proporcionar credenciales alternativas.

> [!Note]  
> No se trata de un "Inicio de sesión en la red" y no implica la recopilación de credenciales.

 

Para obtener información sobre el uso de esta función con un [*proveedor de compatibilidad de seguridad*](../secgloss/s-gly.md) (SSP) específico, vea los temas siguientes.



| Tema                                                                                           | Descripción                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md)<br/>     | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa el proveedor de compatibilidad para seguridad de credenciales (CredSSP).<br/> |
| [**AcquireCredentialsHandle (Resumen)**](acquirecredentialshandle--digest.md)<br/>       | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa la síntesis.<br/>                                         |
| [**AcquireCredentialsHandle (Kerberos)**](acquirecredentialshandle--kerberos.md)<br/>   | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Kerberos.<br/>                                       |
| [**AcquireCredentialsHandle (Negotiate)**](acquirecredentialshandle--negotiate.md)<br/> | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que utiliza Negotiate.<br/>                                      |
| [**AcquireCredentialsHandle (NTLM)**](acquirecredentialshandle--ntlm.md)<br/>           | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa NTLM.<br/>                                           |
| [**AcquireCredentialsHandle (Schannel)**](acquirecredentialshandle--schannel.md)<br/>   | Adquiere un identificador a las credenciales preexistentes de una entidad de seguridad que usa Schannel.<br/>                                       |



 

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

*pszPrincipal* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre de la entidad de seguridad cuyas credenciales hará referencia el identificador.

Cuando se usa el SSP de síntesis, este parámetro es opcional.

Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.

> [!Note]  
> Si el proceso que solicita el identificador no tiene acceso a las credenciales, la función devuelve un error. Una cadena null indica que el proceso requiere un identificador a las credenciales del usuario en cuyo [*contexto de seguridad*](../secgloss/s-gly.md) se está ejecutando.

 

</dd> <dt>

*pszPackage* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del [*paquete de seguridad*](../secgloss/s-gly.md) con el que se utilizarán estas credenciales. Se trata de un nombre de [*paquete de seguridad*](../secgloss/s-gly.md) devuelto en el miembro **Name** de una estructura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) devuelta por la función [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) . Una vez establecido un contexto, se puede llamar a [**QueryContextAttributes (general)**](querycontextattributes--general.md) con *ULATTRIBUTE* establecido en SECPKG \_ ATTR \_ Package \_ info para devolver información sobre el [*paquete de seguridad*](../secgloss/s-gly.md) en uso.

Al usar el SSP de síntesis, establezca este parámetro en WDIGEST \_ Sp \_ Name.

Al usar Schannel SSP, establezca este parámetro en UNISP \_ Name.

</dd> <dt>

*fCredentialUse* \[ de\]
</dt> <dd>

Marca que indica cómo se utilizarán estas credenciales. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <dt>**SECPKG \_ CRED \_ AUTOlogon- \_ Restricted**</dt> <dt>0x00000010</dt> </dl> | La seguridad no usa credenciales de inicio de sesión predeterminadas o credenciales del [Administrador de credenciales](credential-manager.md).<br/> Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)Negotiate.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <dt>**SECPKG \_ CRED \_ both**</dt> </dl>                                                                                                                  | Validar una credencial entrante o usar una credencial local para preparar un token saliente. Esta marca habilita ambos marcadores. Esta marca no es válida con el SSP de Schannel y Digest.<br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <dt>**SECPKG \_ de \_ entrada de cred**</dt> </dl>                                                                                                         | Validar una credencial de servidor entrante. Las credenciales de entrada se pueden validar mediante una autoridad de autenticación cuando se llama a [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) o [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) . Si dicha entidad no está disponible, se producirá un error en la función y se devolverá la \_ \_ autoridad de \_ autenticación \_ . La validación es específica del paquete.<br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <dt>**SECPKG \_ CRED \_ saliente**</dt> </dl>                                                                                                      | Permitir una credencial de cliente local para preparar un token saliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <dt>**SECPKG \_ La \_ Directiva de proceso CRED \_ \_ solo**</dt> es <dt>0x00000020</dt> </dl>   | La función procesa la Directiva de servidor y devuelve las **\_ \_ \_ credenciales sec e no**, lo que indica que la aplicación debe solicitar las credenciales.<br/> Este valor solo es compatible con la [*delegación restringida*](../secgloss/s-gly.md)Negotiate.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                          |



 

</dd> <dt>

*pvLogonID* \[ de\]
</dt> <dd>

Un puntero a un [*identificador local único*](../secgloss/l-gly.md) (LUID) que identifica al usuario. Este parámetro se proporciona para los procesos del sistema de archivos, como los redirectores de red. Este parámetro puede ser **NULL**.

Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.

</dd> <dt>

*pAuthData* \[ de\]
</dt> <dd>

Puntero a datos específicos del paquete. Este parámetro puede ser **null**, lo que indica que se deben usar las credenciales predeterminadas para ese [*paquete de seguridad*](../secgloss/s-gly.md) . Para usar las credenciales proporcionadas, pase una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que incluya esas credenciales en este parámetro. El tiempo de ejecución de RPC pasa todo lo que se proporcionó en [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).

Cuando se usa el SSP de síntesis, este parámetro es un puntero a una estructura de [**\_ identidad de \_ autenticación \_ de WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) de la SEC que contiene la información de autenticación que se va a usar para buscar las credenciales.

Al usar el SSP de Schannel, especifique una estructura de [**\_ CRED de Schannel**](/windows/win32/api/schannel/ns-schannel-schannel_cred) que indique el protocolo que se va a usar y los valores para varias características de canal personalizables.

Al usar los paquetes NTLM o Negotiate, las longitudes máximas de caracteres para el nombre de usuario, la contraseña y el dominio son 256, 256 y 15, respectivamente.

</dd> <dt>

*pGetKeyFn* \[ de\]
</dt> <dd>

Este parámetro no se utiliza y debe establecerse en **null**.

</dd> <dt>

*pvGetKeyArgument* \[ de\]
</dt> <dd>

Este parámetro no se utiliza y debe establecerse en **null**.

</dd> <dt>

*phCredential* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [CredHandle](sspi-handles.md) para recibir el identificador de la credencial.

</dd> <dt>

*ptsExpiry* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [**marca**](timestamp.md) de tiempo que recibe la hora a la que expiran las credenciales devueltas. El valor devuelto en esta estructura de **marca** de tiempo depende de la [*delegación restringida*](../secgloss/s-gly.md). El [*paquete de seguridad*](../secgloss/s-gly.md) debe devolver este valor en la hora local.

Este parámetro se establece en un tiempo máximo constante. No hay ningún tiempo de expiración para las credenciales o el [*contexto de seguridad*](../secgloss/s-gly.md)implícita o cuando se usa el SSP de síntesis.

Cuando se usa Schannel SSP, este parámetro es opcional. Cuando la credencial que se va a usar para la autenticación es un certificado, este parámetro recibe la hora de expiración de ese certificado. Si no se ha proporcionado ningún certificado, se devuelve un valor de tiempo máximo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                 | Descripción                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ memoria insuficiente \_**</dt> </dl> | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                  |
| <dl> <dt>**s \_ E \_ interno \_ error**</dt> </dl>      | Error que no se ha asignado a un código de error SSPI.<br/>                                                                               |
| <dl> <dt>**s \_ E \_ sin \_ credenciales**</dt> </dl>      | No hay credenciales disponibles en la [*delegación restringida*](../secgloss/s-gly.md).<br/> |
| <dl> <dt>**s \_ E \_ no \_ propietario**</dt> </dl>           | El autor de la llamada de la función no tiene las credenciales necesarias.<br/>                                                                     |
| <dl> <dt>**s \_ E \_ SECPKG \_ no \_ encontrados**</dt> </dl>   | El [*paquete de seguridad*](../secgloss/s-gly.md) solicitado no existe.<br/>                                                                                          |
| <dl> <dt>**s \_ E \_ credenciales desconocidas \_**</dt> </dl> | No se reconocieron las credenciales proporcionadas al paquete.<br/>                                                                            |



 

## <a name="remarks"></a>Observaciones

La función **AcquireCredentialsHandle (general)** devuelve un identificador a las credenciales de una entidad de seguridad, como un usuario o un cliente, tal y como lo usa una [*delegación restringida*](../secgloss/s-gly.md)específica. Puede ser el identificador de las credenciales preexistentes o la función puede crear un nuevo conjunto de credenciales y devolverlo. Este identificador se puede utilizar en llamadas posteriores a las funciones [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) y [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) .

En general, **AcquireCredentialsHandle (general)** no permite a un proceso obtener un identificador de las credenciales de otros usuarios que han iniciado sesión en el mismo equipo. Sin embargo, un llamador con \_ el \_ [*privilegio*](../secgloss/s-gly.md) ' TCB name ' tiene la opción de especificar el [*identificador de inicio de sesión*](../secgloss/l-gly.md) (LUID) de cualquier token de sesión de inicio de sesión existente para obtener un identificador de las credenciales de la sesión. Normalmente, se usan en los módulos de modo kernel que deben actuar en nombre de un usuario que ha iniciado sesión.

Un paquete podría llamar a la función en *pGetKeyFn* proporcionada por el transporte de tiempo de ejecución de RPC. Si el transporte no admite la noción de devolución de llamada para recuperar credenciales, este parámetro debe ser **null**.

En el caso de los autores de llamadas en modo kernel, deben tenerse en cuentan las siguientes diferencias:

-   Los dos parámetros de cadena deben ser cadenas [*Unicode*](../secgloss/u-gly.md) .
-   Los valores de búfer deben asignarse en la memoria virtual del proceso, no en el grupo.

Cuando haya terminado de usar las credenciales devueltas, libere la memoria que usan las credenciales mediante una llamada a la función [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Nombres Unicode y ANSI<br/>   | **AcquireCredentialsHandleW** (Unicode) y **AcquireCredentialsHandleA** (ANSI)<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**InitializeSecurityContext (general)**](initializesecuritycontext--general.md)
</dt> <dt>

[**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
