---
description: La propiedad elemento uilevel del objeto de instalador es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores en el espacio de proceso actual.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Propiedad Installer. elemento uilevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653992"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="0c361-103">Propiedad Installer. elemento uilevel</span><span class="sxs-lookup"><span data-stu-id="0c361-103">Installer.UILevel property</span></span>

<span data-ttu-id="0c361-104">La propiedad **elemento uilevel** del objeto de [**instalador**](installer-object.md) es una propiedad de lectura y escritura que indica el tipo de interfaz de usuario que se va a usar al abrir y procesar paquetes posteriores en el espacio de proceso actual.</span><span class="sxs-lookup"><span data-stu-id="0c361-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="0c361-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0c361-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c361-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c361-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="0c361-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0c361-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0c361-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c361-108">Remarks</span></span>



| <span data-ttu-id="0c361-109">Nivel de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="0c361-109">User interface level</span></span>   | <span data-ttu-id="0c361-110">Value</span><span class="sxs-lookup"><span data-stu-id="0c361-110">Value</span></span> | <span data-ttu-id="0c361-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c361-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c361-112">msiUILevelNoChange</span><span class="sxs-lookup"><span data-stu-id="0c361-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="0c361-113">0</span><span class="sxs-lookup"><span data-stu-id="0c361-113">0</span></span>     | <span data-ttu-id="0c361-114">No cambia el nivel de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0c361-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0c361-115">msiUILevelDefault</span><span class="sxs-lookup"><span data-stu-id="0c361-115">msiUILevelDefault</span></span>      | <span data-ttu-id="0c361-116">1</span><span class="sxs-lookup"><span data-stu-id="0c361-116">1</span></span>     | <span data-ttu-id="0c361-117">Usa el nivel de IU predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0c361-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="0c361-118">msiUILevelNone</span><span class="sxs-lookup"><span data-stu-id="0c361-118">msiUILevelNone</span></span>         | <span data-ttu-id="0c361-119">2</span><span class="sxs-lookup"><span data-stu-id="0c361-119">2</span></span>     | <span data-ttu-id="0c361-120">Instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="0c361-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="0c361-121">msiUILevelBasic</span><span class="sxs-lookup"><span data-stu-id="0c361-121">msiUILevelBasic</span></span>        | <span data-ttu-id="0c361-122">3</span><span class="sxs-lookup"><span data-stu-id="0c361-122">3</span></span>     | <span data-ttu-id="0c361-123">Progreso simple y control de errores.</span><span class="sxs-lookup"><span data-stu-id="0c361-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="0c361-124">msiUILevelReduced</span><span class="sxs-lookup"><span data-stu-id="0c361-124">msiUILevelReduced</span></span>      | <span data-ttu-id="0c361-125">4</span><span class="sxs-lookup"><span data-stu-id="0c361-125">4</span></span>     | <span data-ttu-id="0c361-126">La interfaz de usuario creada y los cuadros de diálogo del asistente se han suprimido.</span><span class="sxs-lookup"><span data-stu-id="0c361-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="0c361-127">msiUILevelFull</span><span class="sxs-lookup"><span data-stu-id="0c361-127">msiUILevelFull</span></span>         | <span data-ttu-id="0c361-128">5</span><span class="sxs-lookup"><span data-stu-id="0c361-128">5</span></span>     | <span data-ttu-id="0c361-129">Interfaz de usuario creada con asistentes, progreso y errores.</span><span class="sxs-lookup"><span data-stu-id="0c361-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="0c361-130">msiUILevelHideCancel</span><span class="sxs-lookup"><span data-stu-id="0c361-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="0c361-131">32</span><span class="sxs-lookup"><span data-stu-id="0c361-131">32</span></span>    | <span data-ttu-id="0c361-132">Si se combina con el valor msiUILevelBasic, el instalador muestra cuadros de diálogo de progreso pero no muestra un botón **Cancelar** en el cuadro de diálogo para impedir que los usuarios cancelen la instalación.</span><span class="sxs-lookup"><span data-stu-id="0c361-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="0c361-133">msiUILevelProgressOnly</span><span class="sxs-lookup"><span data-stu-id="0c361-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="0c361-134">64</span><span class="sxs-lookup"><span data-stu-id="0c361-134">64</span></span>    | <span data-ttu-id="0c361-135">Si se combina con el valor msiUILevelBasic, el instalador muestra cuadros de diálogo de progreso pero no muestra cuadros de diálogo modales ni cuadros de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="0c361-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="0c361-136">msiUILevelEndDialog</span><span class="sxs-lookup"><span data-stu-id="0c361-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="0c361-137">128</span><span class="sxs-lookup"><span data-stu-id="0c361-137">128</span></span>   | <span data-ttu-id="0c361-138">Si se combina con cualquier valor anterior, el instalador muestra un cuadro de diálogo modal al final de una instalación correcta o si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="0c361-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="0c361-139">No se muestra ningún cuadro de diálogo si el usuario cancela.</span><span class="sxs-lookup"><span data-stu-id="0c361-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="0c361-140">Vea también [determinar el nivel de interfaz de usuario desde una acción personalizada](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="0c361-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c361-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c361-141">Requirements</span></span>



| <span data-ttu-id="0c361-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c361-142">Requirement</span></span> | <span data-ttu-id="0c361-143">Value</span><span class="sxs-lookup"><span data-stu-id="0c361-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c361-144">Versión</span><span class="sxs-lookup"><span data-stu-id="0c361-144">Version</span></span><br/> | <span data-ttu-id="0c361-145">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c361-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c361-146">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c361-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c361-147">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c361-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0c361-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c361-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c361-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c361-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0c361-150">IID</span><span class="sxs-lookup"><span data-stu-id="0c361-150">IID</span></span><br/>     | <span data-ttu-id="0c361-151">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0c361-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




