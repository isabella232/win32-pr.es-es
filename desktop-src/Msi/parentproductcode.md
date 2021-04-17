---
description: Durante una instalación simultánea, el instalador establece la propiedad ParentProductCode en la sesión de la instalación simultánea en el mismo valor que la propiedad ProductCode en la sesión de la instalación primaria.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Propiedad ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653767"
---
# <a name="parentproductcode-property"></a><span data-ttu-id="4d68e-103">Propiedad ParentProductCode</span><span class="sxs-lookup"><span data-stu-id="4d68e-103">ParentProductCode property</span></span>

<span data-ttu-id="4d68e-104">Durante una instalación simultánea, el instalador establece la propiedad **ParentProductCode** en la sesión de la instalación simultánea en el mismo valor que la propiedad [**ProductCode**](productcode.md) en la sesión de la instalación primaria.</span><span class="sxs-lookup"><span data-stu-id="4d68e-104">During a concurrent installation, the installer sets the **ParentProductCode** property in the concurrent installation's session to the same value as the [**ProductCode**](productcode.md) property in the parent installation's session.</span></span> <span data-ttu-id="4d68e-105">Las instalaciones primarias ejecutan las acciones de instalación simultáneas para realizar una instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="4d68e-105">Parent installations run the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="4d68e-106">Un paquete de instalación puede determinar si se está instalando mediante una acción de instalación simultánea comprobando el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4d68e-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="4d68e-107">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="4d68e-107">Concurrent Installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="4d68e-108">Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.</span><span class="sxs-lookup"><span data-stu-id="4d68e-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="4d68e-109">Esta propiedad no se establece si la acción [RemoveExistingProducts](removeexistingproducts-action.md) ejecuta la instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="4d68e-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="4d68e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d68e-110">Remarks</span></span>

<span data-ttu-id="4d68e-111">Para evitar que un paquete se instale una vez como una instalación simultánea, agregue cualquiera de las siguientes instrucciones condicionales a la tabla [LaunchCondition](launchcondition-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4d68e-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="4d68e-112">Esto evita que el paquete se instale una acción de instalación simultánea ejecutada por otra instalación.</span><span class="sxs-lookup"><span data-stu-id="4d68e-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="4d68e-113">Esto no impide que el paquete se instale mediante la acción [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4d68e-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="4d68e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d68e-114">Requirements</span></span>



| <span data-ttu-id="4d68e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d68e-115">Requirement</span></span> | <span data-ttu-id="4d68e-116">Value</span><span class="sxs-lookup"><span data-stu-id="4d68e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d68e-117">Versión</span><span class="sxs-lookup"><span data-stu-id="4d68e-117">Version</span></span><br/> | <span data-ttu-id="4d68e-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4d68e-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4d68e-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4d68e-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4d68e-120">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4d68e-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4d68e-121">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4d68e-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d68e-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d68e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d68e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d68e-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4d68e-124">**ParentOriginalDatabase**</span><span class="sxs-lookup"><span data-stu-id="4d68e-124">**ParentOriginalDatabase**</span></span>](parentoriginaldatabase.md)
</dt> </dl>

 

 




