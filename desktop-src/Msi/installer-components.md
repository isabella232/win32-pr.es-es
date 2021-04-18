---
description: La propiedad componentes de solo lectura devuelve un objeto StringList que enumera el conjunto de componentes instalados para todos los productos.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653802"
---
# <a name="installercomponents-property"></a><span data-ttu-id="858f3-103">Installer. Components (propiedad)</span><span class="sxs-lookup"><span data-stu-id="858f3-103">Installer.Components property</span></span>

<span data-ttu-id="858f3-104">La propiedad **componentes** de solo lectura devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de componentes instalados para todos los productos.</span><span class="sxs-lookup"><span data-stu-id="858f3-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="858f3-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="858f3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="858f3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="858f3-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="858f3-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="858f3-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="858f3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="858f3-108">Remarks</span></span>

<span data-ttu-id="858f3-109">Para enumerar los componentes, una aplicación puede recorrer en iteración el objeto [**StringList**](stringlist-object.md) mediante una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="858f3-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="858f3-110">Dado que los componentes no están ordenados, los componentes nuevos tienen un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="858f3-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="858f3-111">Esto significa que la función puede devolver componentes en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="858f3-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="858f3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="858f3-112">Requirements</span></span>



| <span data-ttu-id="858f3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="858f3-113">Requirement</span></span> | <span data-ttu-id="858f3-114">Value</span><span class="sxs-lookup"><span data-stu-id="858f3-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="858f3-115">Versión</span><span class="sxs-lookup"><span data-stu-id="858f3-115">Version</span></span><br/> | <span data-ttu-id="858f3-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="858f3-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="858f3-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="858f3-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="858f3-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="858f3-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="858f3-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="858f3-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="858f3-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="858f3-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="858f3-121">IID</span><span class="sxs-lookup"><span data-stu-id="858f3-121">IID</span></span><br/>     | <span data-ttu-id="858f3-122">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="858f3-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="858f3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="858f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="858f3-124">**MsiEnumComponents**</span><span class="sxs-lookup"><span data-stu-id="858f3-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




