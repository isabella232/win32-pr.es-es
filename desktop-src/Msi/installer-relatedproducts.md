---
description: La propiedad Productosrelacionados de solo lectura devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales con una propiedad UpgradeCode especificada en su tabla de propiedades.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Propiedad Installer. Productosrelacionados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653888"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="549a1-103">Propiedad Installer. Productosrelacionados</span><span class="sxs-lookup"><span data-stu-id="549a1-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="549a1-104">La propiedad **productosrelacionados** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales con una propiedad [**UpgradeCode**](upgradecode.md) especificada en su [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="549a1-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="549a1-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="549a1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="549a1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="549a1-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="549a1-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="549a1-107">Property value</span></span>

<span data-ttu-id="549a1-108">El código de actualización de los productos relacionados enumerados por el instalador.</span><span class="sxs-lookup"><span data-stu-id="549a1-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="549a1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="549a1-109">Remarks</span></span>

<span data-ttu-id="549a1-110">Para enumerar los productos relacionados, una aplicación recorre en iteración el [**StringList**](stringlist-object.md) con una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="549a1-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="549a1-111">Dado que los productos relacionados no están ordenados, cualquier nuevo producto relacionado tiene un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="549a1-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="549a1-112">Esto significa que la función puede devolver los productos relacionados en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="549a1-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="549a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="549a1-113">Requirements</span></span>



| <span data-ttu-id="549a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="549a1-114">Requirement</span></span> | <span data-ttu-id="549a1-115">Value</span><span class="sxs-lookup"><span data-stu-id="549a1-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549a1-116">Versión</span><span class="sxs-lookup"><span data-stu-id="549a1-116">Version</span></span><br/> | <span data-ttu-id="549a1-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="549a1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="549a1-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="549a1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="549a1-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="549a1-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="549a1-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="549a1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="549a1-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549a1-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="549a1-122">IID</span><span class="sxs-lookup"><span data-stu-id="549a1-122">IID</span></span><br/>     | <span data-ttu-id="549a1-123">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="549a1-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="549a1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="549a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549a1-125">**MsiEnumRelatedProducts**</span><span class="sxs-lookup"><span data-stu-id="549a1-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




