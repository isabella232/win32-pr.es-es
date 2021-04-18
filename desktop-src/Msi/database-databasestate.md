---
description: La propiedad DatabaseState del objeto de base de datos es una propiedad de solo lectura.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propiedad Database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653489"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="93d6f-103">Propiedad Database. DatabaseState</span><span class="sxs-lookup"><span data-stu-id="93d6f-103">Database.DatabaseState property</span></span>

<span data-ttu-id="93d6f-104">La propiedad **DatabaseState** del objeto de [**base de datos**](database-object.md) es una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93d6f-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="93d6f-105">Esta propiedad devuelve el estado de persistencia de la base de datos como uno de los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="93d6f-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="93d6f-106">Estado de base de datos</span><span class="sxs-lookup"><span data-stu-id="93d6f-106">Database state</span></span>        | <span data-ttu-id="93d6f-107">Value</span><span class="sxs-lookup"><span data-stu-id="93d6f-107">Value</span></span> | <span data-ttu-id="93d6f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="93d6f-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d6f-109">msiDatabaseStateRead</span><span class="sxs-lookup"><span data-stu-id="93d6f-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="93d6f-110">0</span><span class="sxs-lookup"><span data-stu-id="93d6f-110">0</span></span>     | <span data-ttu-id="93d6f-111">La base de datos se abre como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93d6f-111">Database opens as read-only.</span></span> <span data-ttu-id="93d6f-112">No se permiten cambios en los datos persistentes y no se guardan los datos temporales.</span><span class="sxs-lookup"><span data-stu-id="93d6f-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="93d6f-113">msiDatabaseStateWrite</span><span class="sxs-lookup"><span data-stu-id="93d6f-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="93d6f-114">1</span><span class="sxs-lookup"><span data-stu-id="93d6f-114">1</span></span>     | <span data-ttu-id="93d6f-115">La base de datos está totalmente operativa para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="93d6f-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="93d6f-116">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="93d6f-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d6f-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93d6f-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="93d6f-118">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="93d6f-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="93d6f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93d6f-119">Requirements</span></span>



| <span data-ttu-id="93d6f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d6f-120">Requirement</span></span> | <span data-ttu-id="93d6f-121">Value</span><span class="sxs-lookup"><span data-stu-id="93d6f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d6f-122">Versión</span><span class="sxs-lookup"><span data-stu-id="93d6f-122">Version</span></span><br/> | <span data-ttu-id="93d6f-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="93d6f-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="93d6f-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="93d6f-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="93d6f-125">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="93d6f-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="93d6f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93d6f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="93d6f-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93d6f-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="93d6f-128">IID</span><span class="sxs-lookup"><span data-stu-id="93d6f-128">IID</span></span><br/>     | <span data-ttu-id="93d6f-129">IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="93d6f-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




