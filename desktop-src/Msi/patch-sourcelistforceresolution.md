---
description: El método SourceListForceResolution borra la última propiedad de origen utilizada.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Patch. SourceListForceResolution (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653435"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="a0c74-103">Patch. SourceListForceResolution (método)</span><span class="sxs-lookup"><span data-stu-id="a0c74-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="a0c74-104">El método **SourceListForceResolution** borra la última propiedad de origen utilizada.</span><span class="sxs-lookup"><span data-stu-id="a0c74-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="a0c74-105">Esto obliga al instalador a buscar en la lista de origen un origen de revisión válido la próxima vez que se requiera el origen de la revisión.</span><span class="sxs-lookup"><span data-stu-id="a0c74-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="a0c74-106">Por ejemplo, el instalador requiere que el origen de la revisión realice una instalación o reinstalación cuando falta la copia de la caché local de la revisión.</span><span class="sxs-lookup"><span data-stu-id="a0c74-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="a0c74-107">Este método llama a [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="a0c74-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c74-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0c74-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="a0c74-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0c74-109">Parameters</span></span>

<span data-ttu-id="a0c74-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a0c74-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0c74-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0c74-111">Return value</span></span>

<span data-ttu-id="a0c74-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a0c74-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0c74-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0c74-113">Requirements</span></span>



| <span data-ttu-id="a0c74-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0c74-114">Requirement</span></span> | <span data-ttu-id="a0c74-115">Value</span><span class="sxs-lookup"><span data-stu-id="a0c74-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c74-116">Versión</span><span class="sxs-lookup"><span data-stu-id="a0c74-116">Version</span></span><br/> | <span data-ttu-id="a0c74-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a0c74-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a0c74-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a0c74-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a0c74-119">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a0c74-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a0c74-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0c74-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0c74-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0c74-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a0c74-122">IID</span><span class="sxs-lookup"><span data-stu-id="a0c74-122">IID</span></span><br/>     | <span data-ttu-id="a0c74-123">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a0c74-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a0c74-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0c74-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c74-125">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="a0c74-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a0c74-126">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="a0c74-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="a0c74-127">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="a0c74-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




