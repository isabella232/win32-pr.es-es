---
description: El método SourceListForceResolution borra la propiedad LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Product. SourceListForceResolution (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653813"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="4dd30-103">Product. SourceListForceResolution (método)</span><span class="sxs-lookup"><span data-stu-id="4dd30-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="4dd30-104">El método **SourceListForceResolution** borra la propiedad LastUsedSource.</span><span class="sxs-lookup"><span data-stu-id="4dd30-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="4dd30-105">Esto obliga al instalador a buscar en la lista de origen un origen de producto válido la próxima vez que se requiera un origen, como cuando el instalador realiza una instalación o una reinstalación, o cuando se requiere la ruta de acceso de un conjunto de componentes para que se ejecute desde el origen.</span><span class="sxs-lookup"><span data-stu-id="4dd30-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="4dd30-106">Este método llama a [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="4dd30-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd30-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dd30-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="4dd30-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dd30-108">Parameters</span></span>

<span data-ttu-id="4dd30-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4dd30-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4dd30-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dd30-110">Return value</span></span>

<span data-ttu-id="4dd30-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4dd30-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd30-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dd30-112">Requirements</span></span>



| <span data-ttu-id="4dd30-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dd30-113">Requirement</span></span> | <span data-ttu-id="4dd30-114">Value</span><span class="sxs-lookup"><span data-stu-id="4dd30-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd30-115">Versión</span><span class="sxs-lookup"><span data-stu-id="4dd30-115">Version</span></span><br/> | <span data-ttu-id="4dd30-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4dd30-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4dd30-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4dd30-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4dd30-118">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4dd30-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="4dd30-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4dd30-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4dd30-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dd30-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="4dd30-121">IID</span><span class="sxs-lookup"><span data-stu-id="4dd30-121">IID</span></span><br/>     | <span data-ttu-id="4dd30-122">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4dd30-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="4dd30-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dd30-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd30-124">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="4dd30-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="4dd30-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="4dd30-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="4dd30-126">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="4dd30-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




