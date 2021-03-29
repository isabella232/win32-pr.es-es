---
description: El objeto RecordList es una colección de objetos record. Debe comprobar que el objeto RecordList existe y que no está vacío antes de hacer referencia a sus propiedades.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objeto RecordList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680758"
---
# <a name="recordlist-object"></a><span data-ttu-id="b792e-104">Objeto RecordList</span><span class="sxs-lookup"><span data-stu-id="b792e-104">RecordList object</span></span>

<span data-ttu-id="b792e-105">El objeto **RecordList** es una colección de objetos [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b792e-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="b792e-106">Debe comprobar que el objeto **RecordList** existe y que no está vacío antes de hacer referencia a sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="b792e-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="b792e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b792e-107">Members</span></span>

<span data-ttu-id="b792e-108">El objeto **RecordList** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b792e-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="b792e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b792e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b792e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b792e-110">Properties</span></span>

<span data-ttu-id="b792e-111">El objeto **RecordList** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b792e-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="b792e-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b792e-112">Property</span></span>                                     | <span data-ttu-id="b792e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b792e-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="b792e-114">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="b792e-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="b792e-115">Devuelve el número de elementos del objeto **RecordList** .</span><span class="sxs-lookup"><span data-stu-id="b792e-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="b792e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b792e-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="b792e-117">Devuelve un registro de una colección de objetos **RecordList** .</span><span class="sxs-lookup"><span data-stu-id="b792e-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b792e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b792e-118">Requirements</span></span>



| <span data-ttu-id="b792e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b792e-119">Requirement</span></span> | <span data-ttu-id="b792e-120">Value</span><span class="sxs-lookup"><span data-stu-id="b792e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b792e-121">Versión</span><span class="sxs-lookup"><span data-stu-id="b792e-121">Version</span></span><br/> | <span data-ttu-id="b792e-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b792e-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b792e-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b792e-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b792e-124">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="b792e-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b792e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b792e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b792e-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b792e-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b792e-127">IID</span><span class="sxs-lookup"><span data-stu-id="b792e-127">IID</span></span><br/>     | <span data-ttu-id="b792e-128">IID \_ IRecordList se define como 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b792e-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="b792e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b792e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b792e-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="b792e-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="b792e-131">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b792e-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




