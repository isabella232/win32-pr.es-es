---
title: Propiedades de usuario personalizadas de Winnt
description: El proveedor de WinNT pone a disposición las siguientes propiedades personalizadas para la clase User. Se puede tener acceso a ellos a través de los métodos IADs. get y IADs. Put. Para obtener más información, vea la estructura de la información de usuario \_ \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Propiedades de usuario personalizadas de WinNT ADSI
- Proveedor de WinNT ADSI, objeto de usuario, propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995631"
---
# <a name="winnt-custom-user-properties"></a>Propiedades de usuario personalizadas de Winnt

El proveedor de WinNT pone a disposición las siguientes propiedades personalizadas para la clase User. Se puede tener acceso a ellos a través de los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . Para obtener más información, vea la estructura de la [**información de usuario \_ \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .



| Propiedad            | Tipo         | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Unidad de directorio principal del usuario. Es un puntero a una cadena Unicode que especifica la ruta de acceso del directorio principal. La cadena puede ser **null**. Vea el ejemplo de este tema.                                                                                                                                                                                 |
| **ObjectSID**       | Cadena de octeto | SID de objeto del usuario. Para obtener un ejemplo de cómo recuperar el SID del objeto mediante el proveedor de WinNT, vea [SID del objeto (proveedor de WinNT)](object-sid.md)                                                                                                                                                                                                          |
| **Parámetros**      | String       | Parámetros del usuario. Apunta a una cadena Unicode que se reserva para su uso por parte de las aplicaciones. Esta cadena puede ser una cadena nula o puede tener cualquier número de caracteres antes del carácter nulo de terminación. Los productos de Microsoft usan este miembro para almacenar los datos de configuración de usuario. Esta propiedad solo puede ser modificada por una aplicación durante la instalación. |
| **Contraseñas**     | Hora         | Tiempo de duración de la contraseña en uso. Esta propiedad indica el número de segundos que han transcurrido desde que se cambió la contraseña por última vez.                                                                                                                                                                                                                    |
| **PasswordExpired** | Entero      | Indica cuándo ha expirado la contraseña. Cuando se usa get, devuelve cero si la contraseña no ha expirado o es distinto de cero si ha expirado. Vea el ejemplo de este tema.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Entero      | IDENTIFICADOR de grupo principal del usuario, por ejemplo, el identificador del grupo de usuarios del dominio. Vea el ejemplo de este tema.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Entero      | Marca de usuario definida en la [**\_ \_ \_ enumeración de marca de usuario ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Para obtener un ejemplo de cómo usar UserFlags, consulte la [contraseña nunca expira (proveedor de WinNT)](winnt-password-never-expires.md)                                                                                                                                                             |



 

Este ejemplo muestra cómo establecer el directorio de la unidad de disco principal de un usuario.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



En este ejemplo se muestra cómo usar PasswordExpired para obligar a un usuario a cambiar la contraseña en el siguiente inicio de sesión.


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



En este ejemplo se muestra cómo obtener el grupo principal del usuario.


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 