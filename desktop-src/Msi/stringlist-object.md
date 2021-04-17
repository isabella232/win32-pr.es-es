---
description: El objeto StringList es una colección de cadenas. El cliente debe comprobar que el objeto StringList existe y no está vacío antes de hacer referencia a sus propiedades.
ms.assetid: 7021320a-d01a-43e8-90a5-6105a11a4613
title: Objeto StringList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6493b9e1723d46ce290c7472bbcee7eb9ec34725
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680184"
---
# <a name="stringlist-object"></a><span data-ttu-id="cbb45-104">Objeto StringList</span><span class="sxs-lookup"><span data-stu-id="cbb45-104">StringList object</span></span>

<span data-ttu-id="cbb45-105">El objeto **StringList** es una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="cbb45-105">The **StringList** object is a collection of strings.</span></span> <span data-ttu-id="cbb45-106">El cliente debe comprobar que el objeto **StringList** existe y no está vacío antes de hacer referencia a sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbb45-106">The client must verify that the **StringList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="cbb45-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cbb45-107">Members</span></span>

<span data-ttu-id="cbb45-108">El objeto **StringList** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cbb45-108">The **StringList** object has these types of members:</span></span>

-   [<span data-ttu-id="cbb45-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbb45-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbb45-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbb45-110">Properties</span></span>

<span data-ttu-id="cbb45-111">El objeto **StringList** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cbb45-111">The **StringList** object has these properties.</span></span>



| <span data-ttu-id="cbb45-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbb45-112">Property</span></span>                                     | <span data-ttu-id="cbb45-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbb45-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="cbb45-114">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="cbb45-114">**Count**</span></span>](stringlist-count.md)<br/> | <span data-ttu-id="cbb45-115">Devuelve el número de elementos del objeto **StringList** .</span><span class="sxs-lookup"><span data-stu-id="cbb45-115">Returns the number of items in the **StringList** object.</span></span><br/> |
| [<span data-ttu-id="cbb45-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cbb45-116">**Item**</span></span>](stringlist-item.md)<br/>   | <span data-ttu-id="cbb45-117">Devuelve una cadena en la colección de objetos **StringList** .</span><span class="sxs-lookup"><span data-stu-id="cbb45-117">Returns a string in the **StringList** object collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cbb45-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbb45-118">Requirements</span></span>



| <span data-ttu-id="cbb45-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb45-119">Requirement</span></span> | <span data-ttu-id="cbb45-120">Value</span><span class="sxs-lookup"><span data-stu-id="cbb45-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb45-121">Versión</span><span class="sxs-lookup"><span data-stu-id="cbb45-121">Version</span></span><br/> | <span data-ttu-id="cbb45-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cbb45-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cbb45-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cbb45-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cbb45-124">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="cbb45-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cbb45-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbb45-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cbb45-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbb45-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cbb45-127">IID</span><span class="sxs-lookup"><span data-stu-id="cbb45-127">IID</span></span><br/>     | <span data-ttu-id="cbb45-128">IID \_ IStringList se define como 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cbb45-128">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="cbb45-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbb45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb45-130">Ejemplos de scripting Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cbb45-130">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




