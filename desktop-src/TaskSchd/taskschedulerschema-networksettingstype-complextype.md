---
title: Tipo complejo de networkSettingsType
description: Define los elementos que proporcionan los valores que el servicio Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- tipo complejo de networkSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996606"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="9c959-104">Tipo complejo de networkSettingsType</span><span class="sxs-lookup"><span data-stu-id="9c959-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="9c959-105">Define los elementos que proporcionan los valores que el servicio Programador de tareas utiliza para obtener un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="9c959-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9c959-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c959-106">Child elements</span></span>



| <span data-ttu-id="9c959-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c959-107">Element</span></span>                                                              | <span data-ttu-id="9c959-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c959-108">Type</span></span>                                                        | <span data-ttu-id="9c959-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c959-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c959-110">**Sesión**</span><span class="sxs-lookup"><span data-stu-id="9c959-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="9c959-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="9c959-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="9c959-112">Especifica un valor de GUID que identifica un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="9c959-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="9c959-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="9c959-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="9c959-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="9c959-114">nonEmptyString</span></span>                                              | <span data-ttu-id="9c959-115">Especifica el nombre de un perfil de red.</span><span class="sxs-lookup"><span data-stu-id="9c959-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="9c959-116">El nombre se usa para fines de presentación.</span><span class="sxs-lookup"><span data-stu-id="9c959-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="9c959-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c959-117">Requirements</span></span>



| <span data-ttu-id="9c959-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c959-118">Requirement</span></span> | <span data-ttu-id="9c959-119">Value</span><span class="sxs-lookup"><span data-stu-id="9c959-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c959-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c959-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c959-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c959-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c959-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c959-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c959-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c959-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





