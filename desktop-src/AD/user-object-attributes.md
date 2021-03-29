---
title: Atributos de objeto de usuario
description: Un objeto de usuario tiene varios atributos. En esta sección se documentan los atributos clave usados por Windows, las herramientas administrativas y la libreta de direcciones de Windows (WAB). No describe todos los atributos; no se utilizan muchos atributos para el objeto user.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Atributos de objetos de usuario AD
- Usuarios AD, atributos de objeto de usuario
- Objetos AD, User, Attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995053"
---
# <a name="user-object-attributes"></a>Atributos de objeto de usuario

Un objeto de usuario tiene varios atributos. En esta sección se documentan los atributos clave usados por Windows, las herramientas administrativas y la libreta de direcciones de Windows (WAB). No describe todos los atributos; no se utilizan muchos atributos para el objeto user.

Algunos atributos se almacenan en el directorio, como [**CN**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), etc., y se replican en todos los controladores de dominio dentro de un dominio. Un subconjunto de estos atributos también se replica en el catálogo global.

Los atributos no replicados se almacenan en cada controlador de dominio, pero no se replican en ningún otro lugar, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), etc. Los atributos no replicados son atributos que pertenecen a un controlador de dominio determinado. Por ejemplo, **lastLogon** es la última fecha y hora en que el controlador de dominio concreto que devuelve la propiedad validó el inicio de sesión de red del usuario.

Un objeto de usuario también ha construido atributos que no están almacenados en el directorio, pero se calculan mediante el controlador de dominio, como [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), etc.

Los atributos de los objetos de usuario se clasifican como:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Atributos de objeto base
</dt> <dd>

Esta categoría incluye los atributos requeridos para todos los objetos de directorio, como [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), etc.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Asignar nombres a atributos
</dt> <dd>

Esta categoría incluye atributos que se usan para hacer referencia al objeto o identificarlo, como [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), etc. Para obtener más información sobre los atributos de nomenclatura de los objetos de usuario, vea [atributos de asignación de nombres de usuario](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Atributos de seguridad
</dt> <dd>

Esta categoría incluye atributos para el inicio de sesión y el control de acceso. Para obtener más información sobre los atributos de seguridad para los objetos de usuario, consulte [atributos de seguridad de usuario](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Atributos de la libreta de direcciones
</dt> <dd>

Esta categoría incluye atributos para el correo electrónico y los datos de usuario. Para obtener más información acerca de los atributos de la libreta de direcciones para los objetos de usuario, consulte atributos de la [Libreta de direcciones de usuario](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Atributos específicos de la aplicación
</dt> <dd>

Esta categoría incluye datos de configuración específicos del usuario para aplicaciones específicas.

</dd> </dl>

Para obtener más información sobre cómo leer y modificar los atributos de un objeto de usuario, vea [lectura y escritura de atributos de objetos en Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Para obtener más información sobre la clase de usuario, incluida una lista completa de los atributos [**mayContain**](/windows/desktop/ADSchema/a-maycontain) y [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la clase, vea [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Establecer contraseñas

La contraseña de un usuario no se puede modificar directamente porque esto implicaría enviar una contraseña no cifrada a través de la red. Para establecer la contraseña de un usuario, es necesario usar el método [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . El método **IADsUser. ChangePassword** se utiliza cuando la aplicación permite al usuario cambiar su propia contraseña. El método **IADsUser. SetPassword** se utiliza cuando la aplicación permite a un administrador restablecer una contraseña.

 

 