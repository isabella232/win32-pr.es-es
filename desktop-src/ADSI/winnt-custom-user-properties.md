---
title: Propiedades de usuario personalizado de WinNT
description: El proveedor winNT pone a disposición las siguientes propiedades personalizadas para la clase User. Se puede acceder a ellos a través de los métodos IADs.Get e IADs.Put. Para obtener más información, vea la estructura \_ USER INFO \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- ADSI de propiedades de usuario personalizado de WinNT
- ADSI del proveedor WinNT, objeto de usuario, propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e12fc58ff4829f425302c1d13997f2e6c085646b1ace2c3e8ae2ebfb7df6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838395"
---
# <a name="winnt-custom-user-properties"></a>Propiedades de usuario personalizado de WinNT

El proveedor winNT pone a disposición las siguientes propiedades personalizadas para la clase User. Se puede acceder a ellos a través de los [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) Para obtener más información, vea la [**estructura \_ USER INFO \_ 3.**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3)



| Propiedad            | Tipo         | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | Unidad de directorio principal del usuario. Se trata de un puntero a una cadena Unicode que especifica la ruta de acceso del directorio principal. La cadena puede ser **null.** Vea el ejemplo de este tema.                                                                                                                                                                                 |
| **ObjectSID**       | Cadena de octeto | SID de objeto del usuario. Para obtener un ejemplo de cómo recuperar el SID de objeto mediante el proveedor winNT, vea [SID de objeto (proveedor de WinNT).](object-sid.md)                                                                                                                                                                                                          |
| **Parámetros**      | String       | Parámetros del usuario. Apunta a una cadena Unicode que se reserva para su uso por parte de las aplicaciones. Esta cadena puede ser una cadena null o puede tener cualquier número de caracteres antes del carácter nulo de terminación. Los productos de Microsoft usan este miembro para almacenar datos de configuración de usuario. Una aplicación solo puede modificar esta propiedad durante la instalación. |
| **PasswordAge**     | Time         | Duración de la contraseña en uso. Esta propiedad indica el número de segundos transcurridos desde la última vez que se cambió la contraseña.                                                                                                                                                                                                                    |
| **PasswordExpired** | Entero      | Indica cuándo expiró la contraseña. Cuando use Get, devolverá cero si la contraseña no ha expirado o es distinta de cero si ha expirado. Vea el ejemplo de este tema.                                                                                                                                                                                          |
| **PrimaryGroupID**  | Entero      | Identificador de grupo principal del usuario, por ejemplo, identificador de grupo de usuarios de dominio. Vea el ejemplo de este tema.                                                                                                                                                                                                                                                                        |
| **UserFlags**       | Entero      | Marca de usuario definida en [**ADS \_ USER FLAG \_ \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum). Para obtener un ejemplo de cómo usar UserFlags, consulta [Password Never Expires (WinNT Provider) (Contraseña nunca expira [proveedor WinNT]).](winnt-password-never-expires.md)                                                                                                                                                             |



 

En este ejemplo se muestra cómo establecer el directorio de unidad principal de un usuario.


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



 

 