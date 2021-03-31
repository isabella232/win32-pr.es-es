---
title: Tipo complejo de OpcodeListType
description: Define una lista de códigos de operación que se usan para identificar las operaciones de un componente de la aplicación.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- OpcodeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490420"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="9c9e0-104">Tipo complejo de OpcodeListType</span><span class="sxs-lookup"><span data-stu-id="9c9e0-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="9c9e0-105">Define una lista de códigos de operación que se usan para identificar las operaciones de un componente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c9e0-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9c9e0-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c9e0-106">Child elements</span></span>



| <span data-ttu-id="9c9e0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c9e0-107">Element</span></span>                                                             | <span data-ttu-id="9c9e0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c9e0-108">Type</span></span>                                                             | <span data-ttu-id="9c9e0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c9e0-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="9c9e0-110">**Código**</span><span class="sxs-lookup"><span data-stu-id="9c9e0-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="9c9e0-111">**OpcodeType**</span><span class="sxs-lookup"><span data-stu-id="9c9e0-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="9c9e0-112">Define una operación dentro de un componente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c9e0-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9c9e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c9e0-113">Requirements</span></span>



| <span data-ttu-id="9c9e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c9e0-114">Requirement</span></span> | <span data-ttu-id="9c9e0-115">Value</span><span class="sxs-lookup"><span data-stu-id="9c9e0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c9e0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c9e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9e0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c9e0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c9e0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c9e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9e0-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c9e0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





