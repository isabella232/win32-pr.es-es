---
title: Tipo complejo de LevelListType
description: Define una lista de niveles de gravedad que especifican el nivel de detalle de un evento.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- LevelListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493090"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="88986-104">Tipo complejo de LevelListType</span><span class="sxs-lookup"><span data-stu-id="88986-104">LevelListType Complex Type</span></span>

<span data-ttu-id="88986-105">Define una lista de niveles de gravedad que especifican el nivel de detalle de un evento.</span><span class="sxs-lookup"><span data-stu-id="88986-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="88986-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88986-106">Child elements</span></span>



| <span data-ttu-id="88986-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="88986-107">Element</span></span>                                                          | <span data-ttu-id="88986-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="88986-108">Type</span></span>                                                           | <span data-ttu-id="88986-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="88986-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88986-110">**dosis**</span><span class="sxs-lookup"><span data-stu-id="88986-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="88986-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="88986-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="88986-112">Define un valor de gravedad que determina el nivel de detalle de los eventos durante el registro.</span><span class="sxs-lookup"><span data-stu-id="88986-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="88986-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88986-113">Requirements</span></span>



| <span data-ttu-id="88986-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88986-114">Requirement</span></span> | <span data-ttu-id="88986-115">Value</span><span class="sxs-lookup"><span data-stu-id="88986-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88986-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88986-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88986-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88986-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88986-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88986-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88986-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88986-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





