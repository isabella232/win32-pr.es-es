---
title: Tipo complejo de ProcessingErrorDataType
description: Define un error que se produjo al representar los datos de evento para el evento.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- ProcessingErrorDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150785"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="a8b6b-104">Tipo complejo de ProcessingErrorDataType</span><span class="sxs-lookup"><span data-stu-id="a8b6b-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="a8b6b-105">Define un error que se produjo al representar los datos de evento para el evento.</span><span class="sxs-lookup"><span data-stu-id="a8b6b-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="a8b6b-106">Esto puede ocurrir si los datos de evento no coinciden con la definición de plantilla de datos de evento del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a8b6b-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8b6b-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8b6b-107">Child elements</span></span>



| <span data-ttu-id="a8b6b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8b6b-108">Element</span></span>                                                                          | <span data-ttu-id="a8b6b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8b6b-109">Type</span></span>        | <span data-ttu-id="a8b6b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8b6b-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8b6b-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="a8b6b-112">string</span><span class="sxs-lookup"><span data-stu-id="a8b6b-112">string</span></span>      | <span data-ttu-id="a8b6b-113">Nombre del elemento de datos de evento que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="a8b6b-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="a8b6b-114">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="a8b6b-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a8b6b-115">unsignedInt</span></span> | <span data-ttu-id="a8b6b-116">Código de error del error que se produjo al representar los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="a8b6b-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="a8b6b-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="a8b6b-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="a8b6b-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="a8b6b-118">hexBinary</span></span>   | <span data-ttu-id="a8b6b-119">Un BLOB binario que contiene los datos de evento completos.</span><span class="sxs-lookup"><span data-stu-id="a8b6b-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="a8b6b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b6b-120">Requirements</span></span>



| <span data-ttu-id="a8b6b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b6b-121">Requirement</span></span> | <span data-ttu-id="a8b6b-122">Value</span><span class="sxs-lookup"><span data-stu-id="a8b6b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8b6b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b6b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b6b-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b6b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8b6b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8b6b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b6b-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8b6b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





