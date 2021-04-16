---
Description: La propiedad ALLUSERS configura el contexto de instalación del paquete.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Propiedad ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671455"
---
# <a name="allusers-property"></a><span data-ttu-id="6e8e6-103">Propiedad ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="6e8e6-103">ALLUSERS property</span></span>

<span data-ttu-id="6e8e6-104">La propiedad **AllUsers** configura el contexto de instalación del paquete.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="6e8e6-105">El Windows Installer realiza una instalación por usuario o una instalación por equipo en función de los privilegios de acceso del usuario, independientemente de que se requieran privilegios elevados para instalar la aplicación, el valor de la propiedad **AllUsers** , el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) y la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="6e8e6-106">El valor de la propiedad **AllUsers** , en el momento de la instalación, determina el [contexto de instalación](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="6e8e6-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="6e8e6-107">El valor 1 de la propiedad **AllUsers** especifica el contexto de instalación por máquina.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="6e8e6-108">Un valor de propiedad **AllUsers** de una cadena vacía ("") especifica el contexto de instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="6e8e6-109">Si el valor de la propiedad **AllUsers** está establecido en 2, el Windows Installer restablece siempre el valor de la propiedad **AllUsers** en 1 y realiza una instalación por equipo o restablece el valor de la propiedad **AllUsers** en una cadena vacía ("") y realiza una instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="6e8e6-110">El valor ALLUSERS = 2 permite al sistema restablecer el valor de **AllUsers** y el contexto de instalación, en función de los privilegios del usuario y de la versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="6e8e6-111">**Windows 7:** Establezca la propiedad **AllUsers** en 2 para usar la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) para especificar el contexto de instalación.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="6e8e6-112">Establezca la propiedad **MSIINSTALLPERUSER** en una cadena vacía ("") para una instalación por equipo.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="6e8e6-113">Establezca la propiedad **MSIINSTALLPERUSER** en 1 para una instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="6e8e6-114">Si el paquete se ha escrito siguiendo las instrucciones de desarrollo descritas en [creación de un solo paquete](single-package-authoring.md), los usuarios que tengan acceso de usuario podrán instalar en el contexto por usuario sin tener que proporcionar credenciales de UAC.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="6e8e6-115">Si el usuario tiene privilegios de acceso de usuario, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo de UAC.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="6e8e6-116">**Windows Vista:** Establezca la propiedad **AllUsers** en 2 y Windows Installer cumpla con el [*control de cuentas de usuario*](u-gly.md) (UAC).</span><span class="sxs-lookup"><span data-stu-id="6e8e6-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="6e8e6-117">Si el usuario tiene privilegios de acceso de usuario y ALLUSERS = 2, el instalador realiza una instalación por equipo solo si se proporcionan credenciales de administrador al cuadro de diálogo de UAC.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="6e8e6-118">Si UAC está habilitado y no se proporcionan las credenciales de administrador correctas, se produce un error en la instalación y se indica que se requieren privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="6e8e6-119">Si UAC está deshabilitado por la clave del registro, la Directiva de grupo o el panel de control, no se muestra el cuadro de diálogo UAC y se produce un error en la instalación con un error que indica que se requieren privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="6e8e6-120">**Windows XP:** Establezca la propiedad **AllUsers** en 2 y Windows Installer realiza una instalación por usuario si el usuario tiene privilegios de acceso de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="6e8e6-121">Si el valor de la propiedad **AllUsers** no es igual a 2, el Windows Installer omite el valor de la propiedad [**MSIINSTALLPERUSER**](msiinstallperuser.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8e6-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="6e8e6-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e8e6-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="6e8e6-123">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) en github.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="6e8e6-124">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="6e8e6-124">Default Value</span></span>

<span data-ttu-id="6e8e6-125">El contexto de instalación predeterminado recomendado es por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="6e8e6-126">Si no se establece **AllUsers** , el instalador realiza una instalación por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="6e8e6-127">Puede asegurarse de que la propiedad **AllUsers** no se ha establecido estableciendo su valor en una cadena vacía (""), AllUsers = "".</span><span class="sxs-lookup"><span data-stu-id="6e8e6-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="6e8e6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e8e6-128">Remarks</span></span>

<span data-ttu-id="6e8e6-129">El [contexto de instalación](installation-context.md) determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8e6-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="6e8e6-130">El contexto de instalación determina las partes del registro en las que se escriben o se quitan las entradas de la tabla [del registro](registry-table.md) y la [tabla RemoveRegistry](removeregistry-table.md), con-1 en la columna raíz.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8e6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e8e6-131">Requirements</span></span>



| <span data-ttu-id="6e8e6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e8e6-132">Requirement</span></span> | <span data-ttu-id="6e8e6-133">Value</span><span class="sxs-lookup"><span data-stu-id="6e8e6-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8e6-134">Versión</span><span class="sxs-lookup"><span data-stu-id="6e8e6-134">Version</span></span><br/> | <span data-ttu-id="6e8e6-135">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6e8e6-136">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6e8e6-137">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6e8e6-138">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6e8e6-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e8e6-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6e8e6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8e6-140">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e8e6-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6e8e6-141">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="6e8e6-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="6e8e6-142">Contexto de instalación</span><span class="sxs-lookup"><span data-stu-id="6e8e6-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="6e8e6-143">Creación de un solo paquete</span><span class="sxs-lookup"><span data-stu-id="6e8e6-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




