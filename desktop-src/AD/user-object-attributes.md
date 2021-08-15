---
title: Atributos de objeto de usuario
description: Un objeto de usuario tiene varios atributos. En esta sección se documenta los atributos clave que Windows, las herramientas administrativas y Windows address book (WAB). No describe todos los atributos; no se usan muchos atributos para el objeto de usuario.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Atributos de objeto de usuario AD
- Usuarios ad , atributos de objeto de usuario
- Objetos AD, Usuario, Atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a1bb6b347bd55daceb07dfe1fad4adc3e1352afc91ec14018aab6b24615c2b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182634"
---
# <a name="user-object-attributes"></a>Atributos de objeto de usuario

Un objeto de usuario tiene varios atributos. En esta sección se documenta los atributos clave que Windows, las herramientas administrativas y Windows address book (WAB). No describe todos los atributos; no se usan muchos atributos para el objeto de usuario.

Algunos atributos se almacenan en el directorio, como [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID,**](/windows/desktop/ADSchema/a-objectguid)y así sucesivamente, y se replican en todos los controladores de dominio dentro de un dominio. Un subconjunto de estos atributos también se replica en el catálogo global.

Los atributos no replicados se almacenan en cada controlador de dominio, pero no se replican en otro lugar, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon,**](/windows/desktop/ADSchema/a-lastlogon) [**lastLogoff,**](/windows/desktop/ADSchema/a-lastlogoff)y así sucesivamente. Los atributos no replicados son atributos que pertenecen a un controlador de dominio determinado. Por ejemplo, **lastLogon** es la última fecha y hora en que el controlador de dominio concreto que devuelve la propiedad validó el inicio de sesión de red del usuario.

Un objeto de usuario también tiene atributos creados que no están almacenados en el directorio, pero que calcula el controlador de dominio, como [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes,**](/windows/desktop/ADSchema/a-allowedattributes)y así sucesivamente.

Los atributos de los objetos de usuario se clasifican como:

<dl> <dt>

<span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Atributos de objeto base
</dt> <dd>

Esta categoría incluye los atributos necesarios para todos los objetos de directorio, como [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor,**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)y así sucesivamente.

</dd> <dt>

<span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Asignar nombres a atributos
</dt> <dd>

Esta categoría incluye atributos que se usan para hacer referencia al objeto o identificarlo, como [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID,**](/windows/desktop/ADSchema/a-objectguid) [**objectSID,**](/windows/desktop/ADSchema/a-objectsid)y así sucesivamente. Para obtener más información sobre cómo asignar nombres a atributos para objetos de usuario, vea [Atributos de nomenclatura de usuario](naming-properties.md).

</dd> <dt>

<span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Atributos de seguridad
</dt> <dd>

Esta categoría incluye atributos para el inicio de sesión y el control de acceso. Para obtener más información sobre los atributos de seguridad para objetos de usuario, vea [Atributos de seguridad de usuario](security-properties.md).

</dd> <dt>

<span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Atributos de la libreta de direcciones
</dt> <dd>

Esta categoría incluye atributos para el correo electrónico y los datos de usuario. Para obtener más información sobre los atributos de la libreta de direcciones para objetos de usuario, vea [Atributos de la libreta de direcciones de usuario](address-book-properties.md).

</dd> <dt>

<span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Atributos específicos de la aplicación
</dt> <dd>

Esta categoría incluye datos de configuración específicos del usuario para aplicaciones específicas.

</dd> </dl>

Para obtener más información sobre cómo leer y modificar atributos para un objeto de usuario, vea Leer y escribir atributos de objetos [en Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).

Para obtener más información sobre la clase User, incluida una lista completa de los atributos [**mayContain**](/windows/desktop/ADSchema/a-maycontain) y [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la clase , vea [**User**](/windows/desktop/ADSchema/c-user).

## <a name="setting-passwords"></a>Establecimiento de contraseñas

La contraseña de un usuario no se puede modificar directamente porque implicaría el envío de una contraseña sin cifrar a través de la red. Para establecer la contraseña de un usuario, es necesario usar el [**método IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser.SetPassword.**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) El **método IADsUser.ChangePassword** se usa cuando la aplicación permite al usuario cambiar su propia contraseña. El **método IADsUser.SetPassword** se usa cuando la aplicación permite a un administrador restablecer una contraseña.

 

 