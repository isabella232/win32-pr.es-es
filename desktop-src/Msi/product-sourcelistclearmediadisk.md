---
description: El método SourceListClearMediaDisk del objeto Product quita un disco especificado del conjunto de discos registrados para un producto. Acepta el dipatine como parámetro. Este método llama a MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Product. SourceListClearMediaDisk (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653420"
---
# <a name="productsourcelistclearmediadisk-method"></a><span data-ttu-id="30acb-105">Product. SourceListClearMediaDisk (método)</span><span class="sxs-lookup"><span data-stu-id="30acb-105">Product.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="30acb-106">El método **SourceListClearMediaDisk** del objeto [**Product**](product-object.md) quita un disco especificado del conjunto de discos registrados para un producto.</span><span class="sxs-lookup"><span data-stu-id="30acb-106">The **SourceListClearMediaDisk** method of the [**Product**](product-object.md) object removes a specified disk from the set of registered disks for a product.</span></span> <span data-ttu-id="30acb-107">Acepta el *dipatine* como parámetro.</span><span class="sxs-lookup"><span data-stu-id="30acb-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="30acb-108">Este método llama a [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="30acb-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="30acb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30acb-109">Syntax</span></span>


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="30acb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30acb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30acb-111">*Detectaron*</span><span class="sxs-lookup"><span data-stu-id="30acb-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="30acb-112">Este parámetro proporciona el identificador del disco que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="30acb-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30acb-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30acb-113">Return value</span></span>

<span data-ttu-id="30acb-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="30acb-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="30acb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30acb-115">Requirements</span></span>



| <span data-ttu-id="30acb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="30acb-116">Requirement</span></span> | <span data-ttu-id="30acb-117">Value</span><span class="sxs-lookup"><span data-stu-id="30acb-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30acb-118">Versión</span><span class="sxs-lookup"><span data-stu-id="30acb-118">Version</span></span><br/> | <span data-ttu-id="30acb-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30acb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="30acb-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="30acb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="30acb-121">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="30acb-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="30acb-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30acb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="30acb-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30acb-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="30acb-124">IID</span><span class="sxs-lookup"><span data-stu-id="30acb-124">IID</span></span><br/>     | <span data-ttu-id="30acb-125">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="30acb-125">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="30acb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="30acb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30acb-127">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="30acb-127">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="30acb-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="30acb-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="30acb-129">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="30acb-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




