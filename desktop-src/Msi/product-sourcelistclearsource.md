---
description: El método SourceListClearSource quita una red o un origen de dirección URL. Acepta el tipo, el tipo de origen y SourcePath, la ruta de acceso de origen, como parámetros que se van a quitar. Este método llama a MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Product. SourceListClearSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653419"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="f8f56-105">Product. SourceListClearSource (método)</span><span class="sxs-lookup"><span data-stu-id="f8f56-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="f8f56-106">El método **SourceListClearSource** quita una red o un origen de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="f8f56-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="f8f56-107">Acepta el *tipo*, el tipo de origen y *SourcePath*, la ruta de acceso de origen, como parámetros que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="f8f56-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="f8f56-108">Este método llama a [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="f8f56-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f56-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8f56-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="f8f56-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8f56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f56-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="f8f56-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f56-112">Tipo de origen que se va a quitar: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="f8f56-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="f8f56-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="f8f56-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f56-114">Ruta de acceso al origen que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="f8f56-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f56-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f56-115">Return value</span></span>

<span data-ttu-id="f8f56-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f8f56-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f56-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f56-117">Requirements</span></span>



| <span data-ttu-id="f8f56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f56-118">Requirement</span></span> | <span data-ttu-id="f8f56-119">Value</span><span class="sxs-lookup"><span data-stu-id="f8f56-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f56-120">Versión</span><span class="sxs-lookup"><span data-stu-id="f8f56-120">Version</span></span><br/> | <span data-ttu-id="f8f56-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8f56-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8f56-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8f56-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8f56-123">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f8f56-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f8f56-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8f56-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8f56-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8f56-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f8f56-126">IID</span><span class="sxs-lookup"><span data-stu-id="f8f56-126">IID</span></span><br/>     | <span data-ttu-id="f8f56-127">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f8f56-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="f8f56-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8f56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f56-129">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="f8f56-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="f8f56-130">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="f8f56-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="f8f56-131">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="f8f56-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




