---
title: Atributo User-Account-control
description: Marcas que controlan el comportamiento de la cuenta de usuario.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de control de cuentas de usuario
- atributo de userAccountControl esquema de AD
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151707"
---
# <a name="user-account-control-attribute"></a>Atributo User-Account-control

Marcas que controlan el comportamiento de la cuenta de usuario.



| Entrada | Value |
|-------------------|---------------------------------------|
| CN                | Control de cuentas de usuario                  |
| Nombre para mostrar de LDAP | userAccountControl                    |
| Tamaño              | 4 bytes.                              |
| Actualizar privilegio  | El sistema establece este valor.      |
| Frecuencia de actualización  | Cada vez que cambia la Directiva de cuenta. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-ID-GUID    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Sintaxis            | [**Enumeración**](s-enumeration.md)  |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | True                              |
| En el catálogo global      | True                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="remarks"></a>Observaciones

Este valor de atributo puede ser cero o una combinación de uno o varios de los valores siguientes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor hexadecimal</th>
<th>Identifier (definido en iAds. h)</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x00000001</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></td>
<td>Se ejecuta el script de inicio de sesión.</td>
</tr>
<tr class="even">
<td>0x00000002</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></td>
<td>La cuenta de usuario está deshabilitada.</td>
</tr>
<tr class="odd">
<td>0x00000008</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></td>
<td>El directorio particular es obligatorio.</td>
</tr>
<tr class="even">
<td>0x00000010</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></td>
<td>La cuenta está bloqueada actualmente.</td>
</tr>
<tr class="odd">
<td>0x00000020</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></td>
<td>No se requiere una contraseña.</td>
</tr>
<tr class="even">
<td>0x00000040</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></td>
<td>El usuario no puede cambiar la contraseña.
<blockquote>
[!Note]<br />
No se puede asignar la configuración de permisos de PASSWD_CANT_CHANGE modificando directamente el atributo UserAccountControl. Para obtener más información y un ejemplo de código que muestra cómo evitar que un usuario cambie la contraseña, consulte el <a href="/windows/desktop/ADSI/user-cannot-change-password">usuario no puede cambiar la contraseña</a>.
</blockquote>
<br/> :</td>
</tr>
<tr class="odd">
<td>0x00000080</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></td>
<td>El usuario puede enviar una contraseña cifrada.</td>
</tr>
<tr class="even">
<td>0x00000100</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></td>
<td>Se trata de una cuenta para usuarios cuya cuenta principal se encuentra en otro dominio. Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio. También se conoce como cuenta de usuario local.</td>
</tr>
<tr class="odd">
<td>0x00000200</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></td>
<td>Se trata de un tipo de cuenta predeterminado que representa a un usuario típico.</td>
</tr>
<tr class="even">
<td>0x00000800</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></td>
<td>Se trata de un permiso para confiar en la cuenta de un dominio del sistema que confía en otros dominios.</td>
</tr>
<tr class="odd">
<td>0x00001000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></td>
<td>Se trata de una cuenta de equipo para un equipo que es miembro de este dominio.</td>
</tr>
<tr class="even">
<td>0x00002000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></td>
<td>Se trata de una cuenta de equipo para un controlador de dominio de copia de seguridad del sistema que es miembro de este dominio.</td>
</tr>
<tr class="odd">
<td>0x00004000</td>
<td>N/D</td>
<td>No se utiliza.</td>
</tr>
<tr class="even">
<td>0x00008000</td>
<td>N/D</td>
<td>No se utiliza.</td>
</tr>
<tr class="odd">
<td>0x00010000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></td>
<td>La contraseña de esta cuenta nunca expirará.</td>
</tr>
<tr class="even">
<td>0x00020000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></td>
<td>Se trata de una cuenta de inicio de sesión de MNS.</td>
</tr>
<tr class="odd">
<td>0x00040000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></td>
<td>El usuario debe iniciar sesión con una tarjeta inteligente.</td>
</tr>
<tr class="even">
<td>0x00080000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></td>
<td>La cuenta de servicio (cuenta de usuario o de equipo), en la que se ejecuta un servicio, es de confianza para la delegación Kerberos. Cualquier servicio de este tipo puede suplantar a un cliente que solicite el servicio.</td>
</tr>
<tr class="odd">
<td>0x00100000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></td>
<td>El contexto de seguridad del usuario no se delegará a un servicio, incluso si la cuenta de servicio está establecida como de confianza para la delegación Kerberos.</td>
</tr>
<tr class="even">
<td>0x00200000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></td>
<td>Restrinja esta entidad de seguridad para usar solo los tipos de cifrado estándar de cifrado de datos (DES) para las claves.</td>
</tr>
<tr class="odd">
<td>0x00400000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></td>
<td>Esta cuenta no requiere la autenticación previa de Kerberos para el inicio de sesión.</td>
</tr>
<tr class="even">
<td>0x00800000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></td>
<td>La contraseña de usuario ha expirado. El sistema crea esta marca utilizando los datos del atributo <a href="a-pwdlastset.md"><strong>pwd-Last-Set</strong></a> y la Directiva de dominio.</td>
</tr>
<tr class="odd">
<td>0x01000000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></td>
<td>La cuenta está habilitada para la delegación. Se trata de una configuración que depende de la seguridad; las cuentas con esta opción habilitada deben controlarse estrictamente. Esta configuración permite que un servicio que se ejecuta en la cuenta asuma una identidad de cliente y se autentique como ese usuario en otros servidores remotos de la red.</td>
</tr>
</tbody>
</table>



 

