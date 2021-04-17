---
description: La propiedad ComponentQualifiers es una propiedad de solo lectura que devuelve un objeto StringList que enumera el conjunto de calificadores registrados para el componente especificado.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Propiedad Installer. ComponentQualifiers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653692"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="fb4bd-103">Propiedad Installer. ComponentQualifiers</span><span class="sxs-lookup"><span data-stu-id="fb4bd-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="fb4bd-104">La propiedad **ComponentQualifiers** es una propiedad de solo lectura que devuelve un objeto [**StringList**](stringlist-object.md) que enumera el conjunto de calificadores registrados para el componente especificado.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="fb4bd-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb4bd-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="fb4bd-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fb4bd-107">Property value</span></span>

<span data-ttu-id="fb4bd-108">GUID de cadena que representa la categoría de [componente](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb4bd-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4bd-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb4bd-109">Remarks</span></span>

<span data-ttu-id="fb4bd-110">Para enumerar los calificadores, la aplicación recorre en iteración el objeto [**StringList**](stringlist-object.md) con una construcción for each.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="fb4bd-111">Dado que los calificadores no están ordenados, cualquier calificador nuevo tiene un índice arbitrario, lo que significa que la función puede devolver calificadores en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4bd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4bd-112">Requirements</span></span>



| <span data-ttu-id="fb4bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4bd-113">Requirement</span></span> | <span data-ttu-id="fb4bd-114">Value</span><span class="sxs-lookup"><span data-stu-id="fb4bd-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4bd-115">Versión</span><span class="sxs-lookup"><span data-stu-id="fb4bd-115">Version</span></span><br/> | <span data-ttu-id="fb4bd-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fb4bd-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb4bd-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fb4bd-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb4bd-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fb4bd-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb4bd-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb4bd-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4bd-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fb4bd-121">IID</span><span class="sxs-lookup"><span data-stu-id="fb4bd-121">IID</span></span><br/>     | <span data-ttu-id="fb4bd-122">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fb4bd-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="fb4bd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb4bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4bd-124">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="fb4bd-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




