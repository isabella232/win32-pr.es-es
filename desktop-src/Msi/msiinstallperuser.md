---
description: El usuario puede establecer las propiedades MSIINSTALLPERUSER y ALLUSERS en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el Windows Installer instalar un paquete de doble finalidad para el usuario actual o para todos los usuarios del equipo.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propiedad MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653391"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="bc68b-103">Propiedad MSIINSTALLPERUSER</span><span class="sxs-lookup"><span data-stu-id="bc68b-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="bc68b-104">El usuario puede establecer las propiedades **MSIINSTALLPERUSER** y [**AllUsers**](allusers.md) en el momento de la instalación, a través de la interfaz de usuario o en una línea de comandos, para solicitar que el Windows Installer instalar un paquete de doble finalidad para el usuario actual o para todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="bc68b-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="bc68b-105">Para usar la propiedad **MSIINSTALLPERUSER** , el valor de la propiedad [**AllUsers**](allusers.md) debe ser 2 y se debe haber creado el paquete para poder instalarlo en el contexto por usuario o por equipo.</span><span class="sxs-lookup"><span data-stu-id="bc68b-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="bc68b-106">Para obtener información sobre la creación de un paquete de doble propósito, vea creación de un [solo paquete](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="bc68b-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="bc68b-107">Si el valor de la propiedad **AllUsers** no es igual a 2, el valor de la propiedad **MSIINSTALLPERUSER** se omite y no tiene ningún efecto en la instalación.</span><span class="sxs-lookup"><span data-stu-id="bc68b-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="bc68b-108">El valor de la propiedad **MSIINSTALLPERUSER** se omite al instalar el paquete con Windows Installer 4,5 o una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="bc68b-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="bc68b-109">Para solicitar que el Windows Installer instalar el paquete de uso dual en el [contexto de instalación](installation-context.md)por máquina, el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en una cadena vacía ("") y el valor de la propiedad [**AllUsers**](allusers.md) en 2 mediante una interfaz de usuario creada o una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="bc68b-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="bc68b-110">Para solicitar que el Windows Installer instalar el paquete de uso dual en el [contexto de instalación](installation-context.md)por usuario, el usuario puede establecer el valor de la propiedad **MSIINSTALLPERUSER** en 1 y el valor de la propiedad [**AllUsers**](allusers.md) en 2 mediante una interfaz de usuario creada o una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="bc68b-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="bc68b-111">Si el valor de la propiedad [**AllUsers**](allusers.md) no es igual a 2, el Windows Installer omite el valor de la propiedad **MSIINSTALLPERUSER** .</span><span class="sxs-lookup"><span data-stu-id="bc68b-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="bc68b-112">Si Windows Installer instala la aplicación en el contexto por equipo, restablece el valor de la propiedad **AllUsers** en 1.</span><span class="sxs-lookup"><span data-stu-id="bc68b-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="bc68b-113">Si Windows Installer instala la aplicación en el contexto por usuario, restablece el valor de la propiedad **AllUsers** en una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="bc68b-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="bc68b-114">Por lo tanto, las aplicaciones que se han instalado por usuario reciben todas las actualizaciones o reparaciones por usuario y las aplicaciones instaladas por máquina reciben actualizaciones o reparaciones por equipo.</span><span class="sxs-lookup"><span data-stu-id="bc68b-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="bc68b-115">**[Windows Installer 4,5 o anterior](not-supported-in-windows-installer-4-5.md):** las versiones anteriores a Windows Installer 5,0 omiten la propiedad **MSIINSTALLPERUSER** .</span><span class="sxs-lookup"><span data-stu-id="bc68b-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="bc68b-116">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="bc68b-116">Default Value</span></span>

<span data-ttu-id="bc68b-117">El contexto de instalación predeterminado recomendado es por usuario para un paquete de doble finalidad.</span><span class="sxs-lookup"><span data-stu-id="bc68b-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="bc68b-118">Author MSIINSTALLPERUSER = 1 y ALLUSERS = 2 en la [tabla de propiedades](property-table.md) del paquete de doble uso para especificar por usuario como el contexto de instalación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bc68b-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc68b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc68b-119">Remarks</span></span>

<span data-ttu-id="bc68b-120">Puede asegurarse de que la propiedad **MSIINSTALLPERUSER** no se ha establecido estableciendo su valor en una cadena vacía (""), MSIINSTALLPERUSER = "".</span><span class="sxs-lookup"><span data-stu-id="bc68b-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="bc68b-121">El contexto de instalación determina los valores de las propiedades [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)y [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="bc68b-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="bc68b-122">El contexto de instalación determina las partes del registro en las que se escriben o se quitan las entradas de la tabla [del registro](registry-table.md) y la [tabla RemoveRegistry](removeregistry-table.md), con-1 en la columna raíz.</span><span class="sxs-lookup"><span data-stu-id="bc68b-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="bc68b-123">Para obtener información sobre el contexto de instalación, vea [contexto de instalación](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="bc68b-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc68b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc68b-124">Requirements</span></span>



| <span data-ttu-id="bc68b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc68b-125">Requirement</span></span> | <span data-ttu-id="bc68b-126">Value</span><span class="sxs-lookup"><span data-stu-id="bc68b-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc68b-127">Versión</span><span class="sxs-lookup"><span data-stu-id="bc68b-127">Version</span></span><br/> | <span data-ttu-id="bc68b-128">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc68b-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc68b-129">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bc68b-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc68b-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bc68b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc68b-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc68b-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bc68b-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="bc68b-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="bc68b-133">Contexto de instalación</span><span class="sxs-lookup"><span data-stu-id="bc68b-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="bc68b-134">Creación de un solo paquete</span><span class="sxs-lookup"><span data-stu-id="bc68b-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




