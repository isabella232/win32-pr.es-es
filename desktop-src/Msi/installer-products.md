---
description: La propiedad Products es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Propiedad Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653639"
---
# <a name="installerproducts-property"></a><span data-ttu-id="c1dea-103">Propiedad Installer. Products</span><span class="sxs-lookup"><span data-stu-id="c1dea-103">Installer.Products property</span></span>

<span data-ttu-id="c1dea-104">La propiedad **Products** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de todos los productos instalados o anunciados para el usuario y el equipo actuales.</span><span class="sxs-lookup"><span data-stu-id="c1dea-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="c1dea-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1dea-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dea-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1dea-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="c1dea-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c1dea-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c1dea-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1dea-108">Remarks</span></span>

<span data-ttu-id="c1dea-109">Para enumerar los productos, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="c1dea-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="c1dea-110">Dado que los productos no están ordenados, cualquier producto nuevo tiene un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="c1dea-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="c1dea-111">Esto significa que la función puede devolver los productos en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="c1dea-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dea-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1dea-112">Requirements</span></span>



| <span data-ttu-id="c1dea-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dea-113">Requirement</span></span> | <span data-ttu-id="c1dea-114">Value</span><span class="sxs-lookup"><span data-stu-id="c1dea-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dea-115">Versión</span><span class="sxs-lookup"><span data-stu-id="c1dea-115">Version</span></span><br/> | <span data-ttu-id="c1dea-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1dea-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c1dea-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c1dea-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c1dea-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1dea-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c1dea-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1dea-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="c1dea-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1dea-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c1dea-121">IID</span><span class="sxs-lookup"><span data-stu-id="c1dea-121">IID</span></span><br/>     | <span data-ttu-id="c1dea-122">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c1dea-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c1dea-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1dea-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dea-124">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="c1dea-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




