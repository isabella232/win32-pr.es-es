---
description: El instalador establece la propiedad PATCH en una lista de revisiones que se aplican mediante una llamada a MsiApplyPatch, MsiApplyMultiplePatches o la opción de línea de comandos/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653843"
---
# <a name="patch-property"></a><span data-ttu-id="d1205-103">PATCH (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d1205-103">PATCH property</span></span>

<span data-ttu-id="d1205-104">El instalador establece la propiedad **patch** en una lista de revisiones que se aplican mediante una llamada a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) o la opción de [línea de comandos](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="d1205-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="d1205-105">También puede establecer la propiedad **patch** en la línea de comandos mientras instala un paquete mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o la opción de línea de comandos/i.</span><span class="sxs-lookup"><span data-stu-id="d1205-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="d1205-106">El valor de la propiedad **patch** es una lista de las revisiones que se están instalando.</span><span class="sxs-lookup"><span data-stu-id="d1205-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="d1205-107">Cada revisión de la lista se representa mediante la ruta de acceso completa al paquete de la revisión (archivo. msp). Las rutas de acceso completas de la lista se separan mediante signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="d1205-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="d1205-108">**Windows Installer 2,0:** No se admiten varias revisiones.</span><span class="sxs-lookup"><span data-stu-id="d1205-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="d1205-109">Windows Installer 3,0 es necesario para aplicar varias revisiones.</span><span class="sxs-lookup"><span data-stu-id="d1205-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1205-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1205-110">Remarks</span></span>

<span data-ttu-id="d1205-111">Si crea un paquete de revisión mediante [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) puede especificar que una acción o un cuadro de diálogo solo se ejecuten cuando se aplique una revisión determinada.</span><span class="sxs-lookup"><span data-stu-id="d1205-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="d1205-112">Al crear el paquete de revisión, por ejemplo test. MSP, puede crear una imagen actualizada del producto y un archivo de propiedades de creación de revisiones.</span><span class="sxs-lookup"><span data-stu-id="d1205-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="d1205-113">Al crear el archivo de propiedades de creación de revisiones, puede escribir un nombre de propiedad, por ejemplo PATCHFORTEST, en el campo MediaSrcPropName de la tabla [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="d1205-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="d1205-114">Al crear las tablas de secuencia de la imagen actualizada del producto, puede incluir en la columna condición de la tabla de secuencia una instrucción condicional para la acción o el cuadro de diálogo que desea hacer condicional.</span><span class="sxs-lookup"><span data-stu-id="d1205-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="d1205-115">Por ejemplo, puede usar la siguiente instrucción condicional para ejecutar una acción o un cuadro de diálogo solo cuando se está aplicando test. msp.</span><span class="sxs-lookup"><span data-stu-id="d1205-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="d1205-116">PATCH Y PATCHFORTEST Y PATCH >< PATCHFORTEST</span><span class="sxs-lookup"><span data-stu-id="d1205-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="d1205-117">Dado que la propiedad **patch** puede contener varias revisiones, use el operador de subcadena "><" para comprobar la presencia de una revisión determinada en lugar del operador Equals "=".</span><span class="sxs-lookup"><span data-stu-id="d1205-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="d1205-118">Para obtener más información sobre las instrucciones condicionales, vea la sección [Sintaxis de instrucciones condicionales](conditional-statement-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="d1205-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="d1205-119">El instalador establece ambas propiedades si se aplica una lista de revisiones que incluye test. msp.</span><span class="sxs-lookup"><span data-stu-id="d1205-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="d1205-120">Por ejemplo, puede usar la opción de [línea de comandos](command-line-options.md) /p para aplicar una lista de dos revisiones.</span><span class="sxs-lookup"><span data-stu-id="d1205-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="d1205-121">**msiexec/QB/p \\ \\ Scratch \\ Scratch \\ XYZ \\ patches \\ . MSP; \\ \\ Scratch \\ Scratch \\ XYZ \\ bar. MSP**</span><span class="sxs-lookup"><span data-stu-id="d1205-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="d1205-122">El instalador establece las propiedades **patch** y PATCHFORTEST como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="d1205-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="d1205-123">REVISIÓN = \\ \\ borrado de las \\ revisiones XYZ de Scratch \\ \\ \\ . MSP; \\ \\ Scratch \\ Scratch \\ XYZ \\ bar. MSP</span><span class="sxs-lookup"><span data-stu-id="d1205-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="d1205-124">PATCHFORTEST = \\ \\ borrado de las \\ revisiones XYZ de Scratch \\ \\ \\ . MSP</span><span class="sxs-lookup"><span data-stu-id="d1205-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="d1205-125">En este caso, la condición es TRUE y el cuadro de diálogo o acción condicional anterior se puede ejecutar para cada revisión que se está instalando, test. MSP y bar. msp.</span><span class="sxs-lookup"><span data-stu-id="d1205-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="d1205-126">Si no se aplica test. MSP, el instalador no lo incluye en la propiedad **patch** y no establece PATCHFORTEST.</span><span class="sxs-lookup"><span data-stu-id="d1205-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="d1205-127">En este caso, la condición anterior es falsa y la acción condicional o el cuadro de diálogo no se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="d1205-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1205-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1205-128">Requirements</span></span>



| <span data-ttu-id="d1205-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1205-129">Requirement</span></span> | <span data-ttu-id="d1205-130">Value</span><span class="sxs-lookup"><span data-stu-id="d1205-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1205-131">Versión</span><span class="sxs-lookup"><span data-stu-id="d1205-131">Version</span></span><br/> | <span data-ttu-id="d1205-132">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1205-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1205-133">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1205-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1205-134">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d1205-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d1205-135">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d1205-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1205-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d1205-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1205-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1205-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d1205-138">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="d1205-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="d1205-139">Ejemplos de sintaxis de instrucciones condicionales</span><span class="sxs-lookup"><span data-stu-id="d1205-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




