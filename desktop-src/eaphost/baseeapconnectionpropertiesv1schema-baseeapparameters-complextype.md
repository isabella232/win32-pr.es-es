---
title: 'Tipo complejo de BaseEapParameters: propiedades de conexión'
description: Define el elemento de marcador de posición para la configuración específica del método y el tipo de método.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Tipo complejo BaseEapParameters EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105698464"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a><span data-ttu-id="159da-104">Tipo complejo de BaseEapParameters: propiedades de conexión</span><span class="sxs-lookup"><span data-stu-id="159da-104">BaseEapParameters Complex Type - Connection properties</span></span>

<span data-ttu-id="159da-105">El tipo complejo **BaseEapParameters** define el elemento de marcador de posición para la configuración específica del método y el tipo de método.</span><span class="sxs-lookup"><span data-stu-id="159da-105">The **BaseEapParameters** complex type defines the placeholder element for method type and method-specific configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="159da-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="159da-106">Child elements</span></span>



| <span data-ttu-id="159da-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="159da-107">Element</span></span>                                                                            | <span data-ttu-id="159da-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="159da-108">Type</span></span>    | <span data-ttu-id="159da-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="159da-109">Description</span></span>                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [<span data-ttu-id="159da-110">**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="159da-110">**Type**</span></span>](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="159da-111">integer</span><span class="sxs-lookup"><span data-stu-id="159da-111">integer</span></span> | <span data-ttu-id="159da-112">Aquí se permite cualquier instancia del esquema.</span><span class="sxs-lookup"><span data-stu-id="159da-112">Any schema instance is allowed here.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="159da-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="159da-113">Remarks</span></span>

<span data-ttu-id="159da-114">En **BaseEapParameters** , el método puede definir los elementos constituyentes.</span><span class="sxs-lookup"><span data-stu-id="159da-114">In **BaseEapParameters** the method can define the constituent elements.</span></span> <span data-ttu-id="159da-115">El método también realiza la validación de esquemas en los elementos de **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="159da-115">The method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

## <a name="requirements"></a><span data-ttu-id="159da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="159da-116">Requirements</span></span>



| <span data-ttu-id="159da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="159da-117">Requirement</span></span> | <span data-ttu-id="159da-118">Value</span><span class="sxs-lookup"><span data-stu-id="159da-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="159da-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="159da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="159da-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="159da-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="159da-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="159da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="159da-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="159da-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="159da-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="159da-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159da-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="159da-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="159da-125">Esquema baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="159da-125">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





