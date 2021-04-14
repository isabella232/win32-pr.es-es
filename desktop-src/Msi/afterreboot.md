---
description: El instalador establece la propiedad AFTERREBOOT en 1 después de un reinicio invocado por la acción ForceReboot. El instalador agrega AFTERREBOOT = 1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propiedad AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653864"
---
# <a name="afterreboot-property"></a><span data-ttu-id="cb174-104">Propiedad AFTERREBOOT</span><span class="sxs-lookup"><span data-stu-id="cb174-104">AFTERREBOOT property</span></span>

<span data-ttu-id="cb174-105">El instalador establece la propiedad **AFTERREBOOT** en 1 después de un reinicio invocado por la [acción ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb174-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="cb174-106">El instalador agrega AFTERREBOOT = 1 a la línea de comandos que se ejecuta inmediatamente después del reinicio.</span><span class="sxs-lookup"><span data-stu-id="cb174-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb174-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb174-107">Remarks</span></span>

<span data-ttu-id="cb174-108">La [acción ForceReboot](forcereboot-action.md) siempre debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cb174-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="cb174-109">Es posible que se requiera un reinicio si se ha reemplazado un archivo determinado o si se ha instalado un componente determinado.</span><span class="sxs-lookup"><span data-stu-id="cb174-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="cb174-110">El caso es diferente para cada producto y podría ser necesaria una acción personalizada para determinar si es necesario un reinicio.</span><span class="sxs-lookup"><span data-stu-id="cb174-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="cb174-111">Normalmente, la condición de la acción ForceReboot hace uso de la propiedad **AFTERREBOOT** .</span><span class="sxs-lookup"><span data-stu-id="cb174-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb174-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb174-112">Requirements</span></span>



| <span data-ttu-id="cb174-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb174-113">Requirement</span></span> | <span data-ttu-id="cb174-114">Value</span><span class="sxs-lookup"><span data-stu-id="cb174-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb174-115">Versión</span><span class="sxs-lookup"><span data-stu-id="cb174-115">Version</span></span><br/> | <span data-ttu-id="cb174-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb174-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cb174-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb174-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cb174-118">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cb174-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cb174-119">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb174-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb174-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cb174-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb174-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb174-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="cb174-122">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="cb174-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




