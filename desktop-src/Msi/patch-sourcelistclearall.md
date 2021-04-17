---
description: El método SourceListClearAll del objeto patch borra la lista de origen completa de todos los orígenes del tipo especificado para una revisión. Acepta el tipo como parámetro. Este método llama a MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch. SourceListClearAll (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653761"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="2d184-105">Patch. SourceListClearAll (método)</span><span class="sxs-lookup"><span data-stu-id="2d184-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="2d184-106">El método **SourceListClearAll** del objeto [**patch**](patch-object.md) borra la lista de origen completa de todos los orígenes del tipo especificado para una revisión.</span><span class="sxs-lookup"><span data-stu-id="2d184-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="2d184-107">Acepta el *tipo* como parámetro.</span><span class="sxs-lookup"><span data-stu-id="2d184-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="2d184-108">Este método llama a [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span><span class="sxs-lookup"><span data-stu-id="2d184-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d184-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d184-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="2d184-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d184-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d184-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="2d184-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="2d184-112">El tipo de tipo de origen, como red, dirección URL o medio.</span><span class="sxs-lookup"><span data-stu-id="2d184-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d184-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d184-113">Return value</span></span>

<span data-ttu-id="2d184-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2d184-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d184-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d184-115">Requirements</span></span>



| <span data-ttu-id="2d184-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d184-116">Requirement</span></span> | <span data-ttu-id="2d184-117">Value</span><span class="sxs-lookup"><span data-stu-id="2d184-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d184-118">Versión</span><span class="sxs-lookup"><span data-stu-id="2d184-118">Version</span></span><br/> | <span data-ttu-id="2d184-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d184-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d184-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d184-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d184-121">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2d184-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="2d184-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2d184-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d184-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d184-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="2d184-124">IID</span><span class="sxs-lookup"><span data-stu-id="2d184-124">IID</span></span><br/>     | <span data-ttu-id="2d184-125">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2d184-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="2d184-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d184-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d184-127">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="2d184-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="2d184-128">**MsiSourceListClearAllEx**</span><span class="sxs-lookup"><span data-stu-id="2d184-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="2d184-129">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="2d184-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




