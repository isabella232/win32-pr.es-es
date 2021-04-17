---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentOriginalDatabase en la sesión de la instalación simultánea en el mismo valor que la propiedad OriginalDatabase de la sesión de la instalación primaria.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Propiedad ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653768"
---
# <a name="parentoriginaldatabase-property"></a><span data-ttu-id="c586e-103">Propiedad ParentOriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="c586e-103">ParentOriginalDatabase property</span></span>

<span data-ttu-id="c586e-104">Durante una instalación simultánea, el instalador establece la propiedad **ParentOriginalDatabase** en la sesión de la instalación simultánea en el mismo valor que la propiedad [**OriginalDatabase**](originaldatabase.md) de la sesión de la instalación primaria.</span><span class="sxs-lookup"><span data-stu-id="c586e-104">During a concurrent installation, the installer sets the **ParentOriginalDatabase** property in the concurrent installation's session to the same value as the [**OriginalDatabase**](originaldatabase.md) property in the parent installation's session.</span></span> <span data-ttu-id="c586e-105">Las instalaciones primarias usan las acciones de instalación simultáneas para realizar una instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="c586e-105">Parent installations use the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="c586e-106">Un paquete de instalación puede determinar si se está instalando mediante una acción de instalación simultánea comprobando el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c586e-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="c586e-107">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="c586e-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="c586e-108">Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.</span><span class="sxs-lookup"><span data-stu-id="c586e-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="c586e-109">Esta propiedad no se establece si la acción [RemoveExistingProducts](removeexistingproducts-action.md) ejecuta la instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="c586e-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="c586e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c586e-110">Remarks</span></span>

<span data-ttu-id="c586e-111">Para evitar que un paquete se instale una vez como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la tabla [LaunchCondition](launchcondition-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c586e-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="c586e-112">Esto evita que el paquete se instale una acción de instalación simultánea ejecutada por otra instalación.</span><span class="sxs-lookup"><span data-stu-id="c586e-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="c586e-113">Esto no impide que el paquete se instale mediante la acción [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c586e-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="c586e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c586e-114">Requirements</span></span>



| <span data-ttu-id="c586e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c586e-115">Requirement</span></span> | <span data-ttu-id="c586e-116">Value</span><span class="sxs-lookup"><span data-stu-id="c586e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c586e-117">Versión</span><span class="sxs-lookup"><span data-stu-id="c586e-117">Version</span></span><br/> | <span data-ttu-id="c586e-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c586e-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c586e-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c586e-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c586e-120">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c586e-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c586e-121">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c586e-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c586e-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c586e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c586e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c586e-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c586e-124">**ParentProductCode**</span><span class="sxs-lookup"><span data-stu-id="c586e-124">**ParentProductCode**</span></span>](parentproductcode.md)
</dt> </dl>

 

 




