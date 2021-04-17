---
description: La propiedad Features es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de características publicadas para el producto especificado.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Propiedad Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653348"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="4d668-103">Propiedad Installer. Features</span><span class="sxs-lookup"><span data-stu-id="4d668-103">Installer.Features property</span></span>

<span data-ttu-id="4d668-104">La propiedad **Features** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de características publicadas para el producto especificado.</span><span class="sxs-lookup"><span data-stu-id="4d668-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="4d668-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d668-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d668-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d668-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="4d668-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4d668-107">Property value</span></span>

<span data-ttu-id="4d668-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="4d668-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d668-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d668-109">Remarks</span></span>

<span data-ttu-id="4d668-110">Para enumerar las características, una aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="4d668-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="4d668-111">Dado que las características no están ordenadas, todas las características nuevas tienen un índice arbitrario, lo que significa que la función puede devolver características en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="4d668-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d668-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d668-112">Requirements</span></span>



| <span data-ttu-id="4d668-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d668-113">Requirement</span></span> | <span data-ttu-id="4d668-114">Value</span><span class="sxs-lookup"><span data-stu-id="4d668-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d668-115">Versión</span><span class="sxs-lookup"><span data-stu-id="4d668-115">Version</span></span><br/> | <span data-ttu-id="4d668-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4d668-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4d668-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4d668-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4d668-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d668-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4d668-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d668-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4d668-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d668-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4d668-121">IID</span><span class="sxs-lookup"><span data-stu-id="4d668-121">IID</span></span><br/>     | <span data-ttu-id="4d668-122">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4d668-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="4d668-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d668-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d668-124">**MsiEnumFeatures**</span><span class="sxs-lookup"><span data-stu-id="4d668-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="4d668-125">Funciones de estado del sistema</span><span class="sxs-lookup"><span data-stu-id="4d668-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




