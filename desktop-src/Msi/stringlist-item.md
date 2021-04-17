---
description: La propiedad Item es una propiedad de solo lectura que devuelve una cadena en la colección de objetos StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653833"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="04575-103">StringList. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="04575-103">StringList.Item property</span></span>

<span data-ttu-id="04575-104">La propiedad **Item** es una propiedad de solo lectura que devuelve una cadena en la colección de [**objetos StringList**](stringlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="04575-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="04575-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="04575-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04575-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04575-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="04575-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="04575-107">Property value</span></span>

<span data-ttu-id="04575-108">Número de índice del elemento con la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="04575-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="04575-109">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="04575-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="04575-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04575-110">Remarks</span></span>

<span data-ttu-id="04575-111">El cliente debe comprobar que el [**objeto StringList**](stringlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad **Item** .</span><span class="sxs-lookup"><span data-stu-id="04575-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="04575-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04575-112">Requirements</span></span>



| <span data-ttu-id="04575-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="04575-113">Requirement</span></span> | <span data-ttu-id="04575-114">Value</span><span class="sxs-lookup"><span data-stu-id="04575-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04575-115">Versión</span><span class="sxs-lookup"><span data-stu-id="04575-115">Version</span></span><br/> | <span data-ttu-id="04575-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="04575-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="04575-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04575-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="04575-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="04575-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="04575-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04575-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="04575-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04575-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="04575-121">IID</span><span class="sxs-lookup"><span data-stu-id="04575-121">IID</span></span><br/>     | <span data-ttu-id="04575-122">IID \_ IStringList se define como 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="04575-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




