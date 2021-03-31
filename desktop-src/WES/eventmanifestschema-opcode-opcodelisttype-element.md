---
title: OpCode (OpcodeListType) (elemento)
description: Contiene un valor numérico que identifica la actividad o un punto dentro de una actividad que la aplicación estaba realizando cuando generó el evento (por ejemplo, inicialización o cierre).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- elemento OpCode EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151068"
---
# <a name="opcode-opcodelisttype-element"></a><span data-ttu-id="d287e-104">OpCode (OpcodeListType) (elemento)</span><span class="sxs-lookup"><span data-stu-id="d287e-104">opcode (OpcodeListType) Element</span></span>

<span data-ttu-id="d287e-105">Contiene un valor numérico que identifica la actividad o un punto dentro de una actividad que la aplicación estaba realizando cuando generó el evento (por ejemplo, inicialización o cierre).</span><span class="sxs-lookup"><span data-stu-id="d287e-105">Contains a numeric value that identifies the activity or a point within an activity that the application was performing when it raised the event (for example, initialization or closing).</span></span>

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

<span data-ttu-id="d287e-106">El elemento **OpCode** se define mediante el tipo complejo [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d287e-106">The **opcode** element is defined by the [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d287e-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d287e-107">Requirements</span></span>



| <span data-ttu-id="d287e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d287e-108">Requirement</span></span> | <span data-ttu-id="d287e-109">Value</span><span class="sxs-lookup"><span data-stu-id="d287e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d287e-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d287e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d287e-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d287e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d287e-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d287e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d287e-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d287e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d287e-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="d287e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="d287e-115">**Elementos primarios**</span><span class="sxs-lookup"><span data-stu-id="d287e-115">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="d287e-116">**códigos de la (TaskType)**</span><span class="sxs-lookup"><span data-stu-id="d287e-116">**opcodes (TaskType)**</span></span>](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[<span data-ttu-id="d287e-117">**códigos de la (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="d287e-117">**opcodes (ProviderType)**</span></span>](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="d287e-118">**OpCodes (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="d287e-118">**opcodes (MetadataType)**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





