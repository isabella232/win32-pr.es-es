---
description: La presencia de la propiedad MSIINSTANCEGUID indica que un código de producto&\# 8211; el cambio de transformación se registra en el producto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propiedad MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679114"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="c5bab-103">Propiedad MSIINSTANCEGUID</span><span class="sxs-lookup"><span data-stu-id="c5bab-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="c5bab-104">La presencia de la propiedad **MSIINSTANCEGUID** indica que se ha registrado un código de producto que cambia de transformación en el producto.</span><span class="sxs-lookup"><span data-stu-id="c5bab-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="c5bab-105">El valor de la propiedad **MSIINSTANCEGUID** especifica qué instancia de un producto se va a usar para la instalación.</span><span class="sxs-lookup"><span data-stu-id="c5bab-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="c5bab-106">La propiedad **MSIINSTANCEGUID** solo puede hacer referencia a un producto que ya se ha instalado con una transformación de instancia.</span><span class="sxs-lookup"><span data-stu-id="c5bab-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="c5bab-107">Las transformaciones de instancia son código de producto: cambiar las transformaciones disponibles con el instalador que se ejecuta en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5bab-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c5bab-108">Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="c5bab-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bab-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5bab-109">Requirements</span></span>



| <span data-ttu-id="c5bab-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bab-110">Requirement</span></span> | <span data-ttu-id="c5bab-111">Value</span><span class="sxs-lookup"><span data-stu-id="c5bab-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bab-112">Versión</span><span class="sxs-lookup"><span data-stu-id="c5bab-112">Version</span></span><br/> | <span data-ttu-id="c5bab-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5bab-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5bab-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5bab-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5bab-115">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5bab-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c5bab-116">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c5bab-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5bab-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5bab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bab-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c5bab-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c5bab-119">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="c5bab-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




