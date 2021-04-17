---
description: La propiedad MSINEWINSTANCE indica la instalación de una nueva instancia de un producto con transformaciones de instancia.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propiedad MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671204"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="7c4c1-103">Propiedad MSINEWINSTANCE</span><span class="sxs-lookup"><span data-stu-id="7c4c1-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="7c4c1-104">La propiedad **MSINEWINSTANCE** indica la instalación de una nueva instancia de un producto con transformaciones de instancia.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="7c4c1-105">Esta propiedad admite varias instancias a través del código de producto: cambiar transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="7c4c1-106">El valor de esta propiedad es 1.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-106">The value of this property is 1.</span></span> <span data-ttu-id="7c4c1-107">La presencia de esta propiedad en la línea de comandos requiere que la propiedad [**TRANSformations**](transforms.md) también esté presente.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="7c4c1-108">La primera transformación enumerada en **TRANSformaciones** debe ser una transformación de instancia.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="7c4c1-109">Para obtener más información, consulte [instalar varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md) .</span><span class="sxs-lookup"><span data-stu-id="7c4c1-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="7c4c1-110">Esta propiedad está disponible con el instalador que ejecuta un sistema en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4c1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c4c1-111">Requirements</span></span>



| <span data-ttu-id="7c4c1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4c1-112">Requirement</span></span> | <span data-ttu-id="7c4c1-113">Value</span><span class="sxs-lookup"><span data-stu-id="7c4c1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4c1-114">Versión</span><span class="sxs-lookup"><span data-stu-id="7c4c1-114">Version</span></span><br/> | <span data-ttu-id="7c4c1-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7c4c1-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7c4c1-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7c4c1-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7c4c1-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c4c1-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7c4c1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4c1-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c4c1-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7c4c1-121">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7c4c1-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




