---
description: La propiedad Item es una propiedad de solo lectura que devuelve un registro de una colección de objetos RecordList.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList. Item (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670964"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="eb0f2-103">RecordList. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eb0f2-103">RecordList.Item property</span></span>

<span data-ttu-id="eb0f2-104">La propiedad **Item** es una propiedad de solo lectura que devuelve un registro de una colección de objetos [**RecordList**](recordlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="eb0f2-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="eb0f2-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0f2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb0f2-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="eb0f2-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eb0f2-107">Property value</span></span>

<span data-ttu-id="eb0f2-108">Número de índice del elemento con la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="eb0f2-109">El índice es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb0f2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb0f2-110">Remarks</span></span>

<span data-ttu-id="eb0f2-111">El cliente debe comprobar que el objeto [**RecordList**](recordlist-object.md) existe y no está vacío antes de hacer referencia a la propiedad Item.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0f2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb0f2-112">Requirements</span></span>



| <span data-ttu-id="eb0f2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb0f2-113">Requirement</span></span> | <span data-ttu-id="eb0f2-114">Value</span><span class="sxs-lookup"><span data-stu-id="eb0f2-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0f2-115">Versión</span><span class="sxs-lookup"><span data-stu-id="eb0f2-115">Version</span></span><br/> | <span data-ttu-id="eb0f2-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eb0f2-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb0f2-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eb0f2-118">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb0f2-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eb0f2-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb0f2-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb0f2-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb0f2-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eb0f2-121">IID</span><span class="sxs-lookup"><span data-stu-id="eb0f2-121">IID</span></span><br/>     | <span data-ttu-id="eb0f2-122">IID \_ IRecordList se define como 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eb0f2-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




