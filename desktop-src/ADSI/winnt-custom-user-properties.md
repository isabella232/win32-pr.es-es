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
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="c0d84-107">Propiedades de usuario personalizadas de Winnt</span><span class="sxs-lookup"><span data-stu-id="c0d84-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="c0d84-108">El proveedor de WinNT pone a disposición las siguientes propiedades personalizadas para la clase User.</span><span class="sxs-lookup"><span data-stu-id="c0d84-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="c0d84-109">Se puede tener acceso a ellos a través de los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="c0d84-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="c0d84-110">Para obtener más información, vea la estructura de la [**información de usuario \_ \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="c0d84-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="c0d84-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0d84-111">Property</span></span>            | <span data-ttu-id="c0d84-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0d84-112">Type</span></span>         | <span data-ttu-id="c0d84-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0d84-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d84-114">**HomeDirDrive**</span><span class="sxs-lookup"><span data-stu-id="c0d84-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="c0d84-115">String</span><span class="sxs-lookup"><span data-stu-id="c0d84-115">String</span></span>       | <span data-ttu-id="c0d84-116">Unidad de directorio principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="c0d84-117">Es un puntero a una cadena Unicode que especifica la ruta de acceso del directorio principal.</span><span class="sxs-lookup"><span data-stu-id="c0d84-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="c0d84-118">La cadena puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c0d84-118">The string can be **null**.</span></span> <span data-ttu-id="c0d84-119">Vea el ejemplo de este tema.</span><span class="sxs-lookup"><span data-stu-id="c0d84-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c0d84-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="c0d84-120">**ObjectSID**</span></span>       | <span data-ttu-id="c0d84-121">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="c0d84-121">Octet String</span></span> | <span data-ttu-id="c0d84-122">SID de objeto del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-122">Object SID of the user.</span></span> <span data-ttu-id="c0d84-123">Para obtener un ejemplo de cómo recuperar el SID del objeto mediante el proveedor de WinNT, vea [SID del objeto (proveedor de WinNT)](object-sid.md)</span><span class="sxs-lookup"><span data-stu-id="c0d84-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="c0d84-124">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="c0d84-124">**Parameters**</span></span>      | <span data-ttu-id="c0d84-125">String</span><span class="sxs-lookup"><span data-stu-id="c0d84-125">String</span></span>       | <span data-ttu-id="c0d84-126">Parámetros del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-126">Parameters of the user.</span></span> <span data-ttu-id="c0d84-127">Apunta a una cadena Unicode que se reserva para su uso por parte de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c0d84-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="c0d84-128">Esta cadena puede ser una cadena nula o puede tener cualquier número de caracteres antes del carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="c0d84-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="c0d84-129">Los productos de Microsoft usan este miembro para almacenar los datos de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="c0d84-130">Esta propiedad solo puede ser modificada por una aplicación durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="c0d84-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="c0d84-131">**Contraseñas**</span><span class="sxs-lookup"><span data-stu-id="c0d84-131">**PasswordAge**</span></span>     | <span data-ttu-id="c0d84-132">Hora</span><span class="sxs-lookup"><span data-stu-id="c0d84-132">Time</span></span>         | <span data-ttu-id="c0d84-133">Tiempo de duración de la contraseña en uso.</span><span class="sxs-lookup"><span data-stu-id="c0d84-133">Time duration of the password in use.</span></span> <span data-ttu-id="c0d84-134">Esta propiedad indica el número de segundos que han transcurrido desde que se cambió la contraseña por última vez.</span><span class="sxs-lookup"><span data-stu-id="c0d84-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="c0d84-135">**PasswordExpired**</span><span class="sxs-lookup"><span data-stu-id="c0d84-135">**PasswordExpired**</span></span> | <span data-ttu-id="c0d84-136">Entero</span><span class="sxs-lookup"><span data-stu-id="c0d84-136">Integer</span></span>      | <span data-ttu-id="c0d84-137">Indica cuándo ha expirado la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c0d84-137">Tells when the password was expired.</span></span> <span data-ttu-id="c0d84-138">Cuando se usa get, devuelve cero si la contraseña no ha expirado o es distinto de cero si ha expirado.</span><span class="sxs-lookup"><span data-stu-id="c0d84-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="c0d84-139">Vea el ejemplo de este tema.</span><span class="sxs-lookup"><span data-stu-id="c0d84-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c0d84-140">**PrimaryGroupID**</span><span class="sxs-lookup"><span data-stu-id="c0d84-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="c0d84-141">Entero</span><span class="sxs-lookup"><span data-stu-id="c0d84-141">Integer</span></span>      | <span data-ttu-id="c0d84-142">IDENTIFICADOR de grupo principal del usuario, por ejemplo, el identificador del grupo de usuarios del dominio.</span><span class="sxs-lookup"><span data-stu-id="c0d84-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="c0d84-143">Vea el ejemplo de este tema.</span><span class="sxs-lookup"><span data-stu-id="c0d84-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c0d84-144">**UserFlags**</span><span class="sxs-lookup"><span data-stu-id="c0d84-144">**UserFlags**</span></span>       | <span data-ttu-id="c0d84-145">Entero</span><span class="sxs-lookup"><span data-stu-id="c0d84-145">Integer</span></span>      | <span data-ttu-id="c0d84-146">Marca de usuario definida en la [**\_ \_ \_ enumeración de marca de usuario ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span><span class="sxs-lookup"><span data-stu-id="c0d84-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="c0d84-147">Para obtener un ejemplo de cómo usar UserFlags, consulte la [contraseña nunca expira (proveedor de WinNT)](winnt-password-never-expires.md)</span><span class="sxs-lookup"><span data-stu-id="c0d84-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="c0d84-148">Este ejemplo muestra cómo establecer el directorio de la unidad de disco principal de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="c0d84-149">En este ejemplo se muestra cómo usar PasswordExpired para obligar a un usuario a cambiar la contraseña en el siguiente inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0d84-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="c0d84-150">En este ejemplo se muestra cómo obtener el grupo principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0d84-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 