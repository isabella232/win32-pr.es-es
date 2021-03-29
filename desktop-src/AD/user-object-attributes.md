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
# <a name="user-object-attributes"></a><span data-ttu-id="dc770-108">Atributos de objeto de usuario</span><span class="sxs-lookup"><span data-stu-id="dc770-108">User Object Attributes</span></span>

<span data-ttu-id="dc770-109">Un objeto de usuario tiene varios atributos.</span><span class="sxs-lookup"><span data-stu-id="dc770-109">A user object has multiple attributes.</span></span> <span data-ttu-id="dc770-110">En esta sección se documentan los atributos clave usados por Windows, las herramientas administrativas y la libreta de direcciones de Windows (WAB).</span><span class="sxs-lookup"><span data-stu-id="dc770-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="dc770-111">No describe todos los atributos; no se utilizan muchos atributos para el objeto user.</span><span class="sxs-lookup"><span data-stu-id="dc770-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="dc770-112">Algunos atributos se almacenan en el directorio, como [**CN**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), etc., y se replican en todos los controladores de dominio dentro de un dominio.</span><span class="sxs-lookup"><span data-stu-id="dc770-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="dc770-113">Un subconjunto de estos atributos también se replica en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="dc770-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="dc770-114">Los atributos no replicados se almacenan en cada controlador de dominio, pero no se replican en ningún otro lugar, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), etc.</span><span class="sxs-lookup"><span data-stu-id="dc770-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="dc770-115">Los atributos no replicados son atributos que pertenecen a un controlador de dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="dc770-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="dc770-116">Por ejemplo, **lastLogon** es la última fecha y hora en que el controlador de dominio concreto que devuelve la propiedad validó el inicio de sesión de red del usuario.</span><span class="sxs-lookup"><span data-stu-id="dc770-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="dc770-117">Un objeto de usuario también ha construido atributos que no están almacenados en el directorio, pero se calculan mediante el controlador de dominio, como [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), etc.</span><span class="sxs-lookup"><span data-stu-id="dc770-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="dc770-118">Los atributos de los objetos de usuario se clasifican como:</span><span class="sxs-lookup"><span data-stu-id="dc770-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="dc770-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Atributos de objeto base</span><span class="sxs-lookup"><span data-stu-id="dc770-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="dc770-120">Esta categoría incluye los atributos requeridos para todos los objetos de directorio, como [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), etc.</span><span class="sxs-lookup"><span data-stu-id="dc770-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="dc770-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Asignar nombres a atributos</span><span class="sxs-lookup"><span data-stu-id="dc770-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="dc770-122">Esta categoría incluye atributos que se usan para hacer referencia al objeto o identificarlo, como [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), etc.</span><span class="sxs-lookup"><span data-stu-id="dc770-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="dc770-123">Para obtener más información sobre los atributos de nomenclatura de los objetos de usuario, vea [atributos de asignación de nombres de usuario](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dc770-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc770-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Atributos de seguridad</span><span class="sxs-lookup"><span data-stu-id="dc770-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="dc770-125">Esta categoría incluye atributos para el inicio de sesión y el control de acceso.</span><span class="sxs-lookup"><span data-stu-id="dc770-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="dc770-126">Para obtener más información sobre los atributos de seguridad para los objetos de usuario, consulte [atributos de seguridad de usuario](security-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dc770-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc770-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Atributos de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="dc770-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="dc770-128">Esta categoría incluye atributos para el correo electrónico y los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="dc770-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="dc770-129">Para obtener más información acerca de los atributos de la libreta de direcciones para los objetos de usuario, consulte atributos de la [Libreta de direcciones de usuario](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dc770-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc770-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Atributos específicos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="dc770-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="dc770-131">Esta categoría incluye datos de configuración específicos del usuario para aplicaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="dc770-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="dc770-132">Para obtener más información sobre cómo leer y modificar los atributos de un objeto de usuario, vea [lectura y escritura de atributos de objetos en Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="dc770-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="dc770-133">Para obtener más información sobre la clase de usuario, incluida una lista completa de los atributos [**mayContain**](/windows/desktop/ADSchema/a-maycontain) y [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la clase, vea [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="dc770-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="dc770-134">Establecer contraseñas</span><span class="sxs-lookup"><span data-stu-id="dc770-134">Setting Passwords</span></span>

<span data-ttu-id="dc770-135">La contraseña de un usuario no se puede modificar directamente porque esto implicaría enviar una contraseña no cifrada a través de la red.</span><span class="sxs-lookup"><span data-stu-id="dc770-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="dc770-136">Para establecer la contraseña de un usuario, es necesario usar el método [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) o [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="dc770-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="dc770-137">El método **IADsUser. ChangePassword** se utiliza cuando la aplicación permite al usuario cambiar su propia contraseña.</span><span class="sxs-lookup"><span data-stu-id="dc770-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="dc770-138">El método **IADsUser. SetPassword** se utiliza cuando la aplicación permite a un administrador restablecer una contraseña.</span><span class="sxs-lookup"><span data-stu-id="dc770-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 