---
description: La propiedad MsiHiddenProperties se puede usar para impedir que el instalador muestre contraseñas u otra información confidencial en el archivo de registro.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propiedad MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671049"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="31960-103">Propiedad MsiHiddenProperties</span><span class="sxs-lookup"><span data-stu-id="31960-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="31960-104">La propiedad **MsiHiddenProperties** se puede usar para impedir que el instalador muestre contraseñas u otra información confidencial en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="31960-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="31960-105">Para evitar que una propiedad se escriba en el archivo de registro, establezca el valor de la propiedad **MsiHiddenProperties** en el nombre de la propiedad que desea ocultar.</span><span class="sxs-lookup"><span data-stu-id="31960-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="31960-106">Puede ocultar varias propiedades si especifica una cadena de nombres de propiedad delimitados por punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="31960-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="31960-107">Cuando la Directiva de [depuración](debug.md) está establecida en un valor de 7, el instalador escribe la información especificada en una línea de comandos en el registro.</span><span class="sxs-lookup"><span data-stu-id="31960-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="31960-108">Esto hace que las propiedades públicas escritas en una línea de comandos sean visibles aunque la propiedad esté incluida en la propiedad **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="31960-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="31960-109">Esto puede hacer que la información confidencial especificada en una línea de comandos esté visible en el registro.</span><span class="sxs-lookup"><span data-stu-id="31960-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="31960-110">Para obtener más información, vea [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="31960-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31960-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31960-111">Requirements</span></span>



| <span data-ttu-id="31960-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="31960-112">Requirement</span></span> | <span data-ttu-id="31960-113">Value</span><span class="sxs-lookup"><span data-stu-id="31960-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31960-114">Versión</span><span class="sxs-lookup"><span data-stu-id="31960-114">Version</span></span><br/> | <span data-ttu-id="31960-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="31960-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="31960-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="31960-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="31960-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31960-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="31960-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="31960-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31960-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="31960-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31960-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31960-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




