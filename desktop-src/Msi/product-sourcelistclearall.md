---
description: El método SourceListClearAll el objeto Product quita todos los orígenes del producto. Se puede especificar el tipo de origen que se va a quitar.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Product. SourceListClearAll (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653421"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="5d84a-104">Product. SourceListClearAll (método)</span><span class="sxs-lookup"><span data-stu-id="5d84a-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="5d84a-105">El método **SourceListClearAll** el objeto [**Product**](product-object.md) quita todos los orígenes del producto.</span><span class="sxs-lookup"><span data-stu-id="5d84a-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="5d84a-106">Se puede especificar el tipo de origen que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5d84a-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d84a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d84a-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="5d84a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d84a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d84a-109">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="5d84a-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="5d84a-110">Tipo de origen que se va a quitar: MSISOURCETYPE \_ media, MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="5d84a-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d84a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d84a-111">Return value</span></span>

<span data-ttu-id="5d84a-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5d84a-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d84a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d84a-113">Requirements</span></span>



| <span data-ttu-id="5d84a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d84a-114">Requirement</span></span> | <span data-ttu-id="5d84a-115">Value</span><span class="sxs-lookup"><span data-stu-id="5d84a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d84a-116">Versión</span><span class="sxs-lookup"><span data-stu-id="5d84a-116">Version</span></span><br/> | <span data-ttu-id="5d84a-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d84a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d84a-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d84a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d84a-119">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5d84a-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5d84a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d84a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d84a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d84a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5d84a-122">IID</span><span class="sxs-lookup"><span data-stu-id="5d84a-122">IID</span></span><br/>     | <span data-ttu-id="5d84a-123">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d84a-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="5d84a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d84a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d84a-125">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="5d84a-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="5d84a-126">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="5d84a-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="5d84a-127">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="5d84a-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




