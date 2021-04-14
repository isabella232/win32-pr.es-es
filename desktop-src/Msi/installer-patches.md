---
description: La propiedad patches de solo lectura del objeto Installer devuelve un objeto StringList que contiene todas las revisiones aplicadas al producto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Propiedad Installer. patches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653897"
---
# <a name="installerpatches-property"></a><span data-ttu-id="b350a-103">Propiedad Installer. patches</span><span class="sxs-lookup"><span data-stu-id="b350a-103">Installer.Patches property</span></span>

<span data-ttu-id="b350a-104">La propiedad **patches** de solo lectura del objeto [**Installer**](installer-object.md) devuelve un objeto [**StringList**](stringlist-object.md) que contiene todas las revisiones aplicadas al producto.</span><span class="sxs-lookup"><span data-stu-id="b350a-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="b350a-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b350a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b350a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b350a-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="b350a-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b350a-107">Property value</span></span>

<span data-ttu-id="b350a-108">Especifica el código de producto.</span><span class="sxs-lookup"><span data-stu-id="b350a-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b350a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b350a-109">Remarks</span></span>

<span data-ttu-id="b350a-110">Para enumerar las revisiones, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) con una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="b350a-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="b350a-111">Dado que las revisiones no están ordenadas, las nuevas revisiones tienen un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="b350a-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="b350a-112">Esto significa que la función puede devolver revisiones en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="b350a-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="b350a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b350a-113">Requirements</span></span>



| <span data-ttu-id="b350a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b350a-114">Requirement</span></span> | <span data-ttu-id="b350a-115">Value</span><span class="sxs-lookup"><span data-stu-id="b350a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b350a-116">Versión</span><span class="sxs-lookup"><span data-stu-id="b350a-116">Version</span></span><br/> | <span data-ttu-id="b350a-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b350a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b350a-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b350a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b350a-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="b350a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b350a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b350a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b350a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b350a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b350a-122">IID</span><span class="sxs-lookup"><span data-stu-id="b350a-122">IID</span></span><br/>     | <span data-ttu-id="b350a-123">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b350a-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="b350a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b350a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b350a-125">**MsiEnumPatches**</span><span class="sxs-lookup"><span data-stu-id="b350a-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




