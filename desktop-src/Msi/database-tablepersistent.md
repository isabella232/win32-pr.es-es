---
description: La propiedad TablePersistent del objeto de base de datos devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propiedad Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671679"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="3006c-103">Propiedad Database. TablePersistent</span><span class="sxs-lookup"><span data-stu-id="3006c-103">Database.TablePersistent property</span></span>

<span data-ttu-id="3006c-104">La propiedad **TablePersistent** del objeto de [**base de datos**](database-object.md) devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="3006c-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="3006c-105">Estado de tabla</span><span class="sxs-lookup"><span data-stu-id="3006c-105">Table state</span></span>               | <span data-ttu-id="3006c-106">Value</span><span class="sxs-lookup"><span data-stu-id="3006c-106">Value</span></span> | <span data-ttu-id="3006c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3006c-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="3006c-108">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="3006c-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="3006c-109">0</span><span class="sxs-lookup"><span data-stu-id="3006c-109">0</span></span>     | <span data-ttu-id="3006c-110">La tabla es temporal.</span><span class="sxs-lookup"><span data-stu-id="3006c-110">Table is temporary.</span></span>            |
| <span data-ttu-id="3006c-111">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="3006c-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="3006c-112">1</span><span class="sxs-lookup"><span data-stu-id="3006c-112">1</span></span>     | <span data-ttu-id="3006c-113">La tabla es persistente.</span><span class="sxs-lookup"><span data-stu-id="3006c-113">Table is persistent.</span></span>           |
| <span data-ttu-id="3006c-114">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="3006c-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="3006c-115">2</span><span class="sxs-lookup"><span data-stu-id="3006c-115">2</span></span>     | <span data-ttu-id="3006c-116">La tabla no está en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3006c-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="3006c-117">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="3006c-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="3006c-118">3</span><span class="sxs-lookup"><span data-stu-id="3006c-118">3</span></span>     | <span data-ttu-id="3006c-119">Falta el nombre de tabla o no es válido.</span><span class="sxs-lookup"><span data-stu-id="3006c-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="3006c-120">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3006c-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3006c-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3006c-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="3006c-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3006c-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3006c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3006c-123">Requirements</span></span>



| <span data-ttu-id="3006c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3006c-124">Requirement</span></span> | <span data-ttu-id="3006c-125">Value</span><span class="sxs-lookup"><span data-stu-id="3006c-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3006c-126">Versión</span><span class="sxs-lookup"><span data-stu-id="3006c-126">Version</span></span><br/> | <span data-ttu-id="3006c-127">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3006c-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3006c-128">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3006c-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3006c-129">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3006c-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3006c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3006c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="3006c-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3006c-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3006c-132">IID</span><span class="sxs-lookup"><span data-stu-id="3006c-132">IID</span></span><br/>     | <span data-ttu-id="3006c-133">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3006c-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




