---
title: Tipo simple de processTokenSidType
description: Define los valores posibles para el elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Programador de tareas de tipo simple processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422161"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="29a32-104">Tipo simple de processTokenSidType</span><span class="sxs-lookup"><span data-stu-id="29a32-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="29a32-105">Define los valores posibles para el elemento [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="29a32-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="29a32-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="29a32-106">Enumeration values</span></span>

<span data-ttu-id="29a32-107">El tipo simple **processTokenSidType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="29a32-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="29a32-108">Value</span><span class="sxs-lookup"><span data-stu-id="29a32-108">Value</span></span>        | <span data-ttu-id="29a32-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="29a32-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a32-110">None</span><span class="sxs-lookup"><span data-stu-id="29a32-110">None</span></span>         | <span data-ttu-id="29a32-111">Las tareas se ejecutan en un proceso que no contiene un SID de token de proceso (no se realizarán cambios en la lista de grupos de tokens de proceso).</span><span class="sxs-lookup"><span data-stu-id="29a32-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="29a32-112">Sin restricciones</span><span class="sxs-lookup"><span data-stu-id="29a32-112">Unrestricted</span></span> | <span data-ttu-id="29a32-113">Un SID de tarea se derivará de la ruta de acceso completa de la tarea y se agregará a la lista de grupos de tokens de proceso.</span><span class="sxs-lookup"><span data-stu-id="29a32-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="29a32-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29a32-114">Requirements</span></span>



| <span data-ttu-id="29a32-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29a32-115">Requirement</span></span> | <span data-ttu-id="29a32-116">Value</span><span class="sxs-lookup"><span data-stu-id="29a32-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="29a32-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29a32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29a32-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="29a32-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="29a32-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29a32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29a32-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="29a32-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





