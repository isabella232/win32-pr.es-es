---
title: 'Tipo complejo de BaseEapParameters: propiedades de usuario'
description: Define el elemento que especificó las credenciales seleccionadas del método heredado y específicas del método.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718577"
---
# <a name="baseeapparameters-complex-type---user-properties"></a><span data-ttu-id="83142-104">Tipo complejo de BaseEapParameters: propiedades de usuario</span><span class="sxs-lookup"><span data-stu-id="83142-104">BaseEapParameters Complex Type - User properties</span></span>

<span data-ttu-id="83142-105">El tipo complejo **BaseEapParameters** define el elemento que especificó las credenciales seleccionadas del método heredado y específicas del método.</span><span class="sxs-lookup"><span data-stu-id="83142-105">The **BaseEapParameters** complex type defines the element that specified the legacy method selected and method-specific credentials.</span></span>

<span data-ttu-id="83142-106">El método puede definir los elementos constituyentes dentro de **BaseEapParameters**; el método también realiza la validación de esquemas en los elementos de **BaseEapParameters**.</span><span class="sxs-lookup"><span data-stu-id="83142-106">The method can define the constituent elements inside **BaseEapParameters**; the method also performs schema validation on the elements in **BaseEapParameters**.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="83142-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83142-107">Child elements</span></span>



| <span data-ttu-id="83142-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="83142-108">Element</span></span>                                                                      | <span data-ttu-id="83142-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="83142-109">Type</span></span>    | <span data-ttu-id="83142-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="83142-110">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83142-111">**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="83142-111">**Type**</span></span>](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | <span data-ttu-id="83142-112">integer</span><span class="sxs-lookup"><span data-stu-id="83142-112">integer</span></span> | <span data-ttu-id="83142-113">Define el elemento de marcador de posición para el tipo de método seleccionado y las credenciales específicas del método.</span><span class="sxs-lookup"><span data-stu-id="83142-113">Defines the placeholder element for the method type selected and method specific credentials.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="83142-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83142-114">Requirements</span></span>



| <span data-ttu-id="83142-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83142-115">Requirement</span></span> | <span data-ttu-id="83142-116">Value</span><span class="sxs-lookup"><span data-stu-id="83142-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83142-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83142-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83142-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83142-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="83142-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83142-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83142-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="83142-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83142-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="83142-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83142-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="83142-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="83142-123">Esquema baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="83142-123">baseeapuserpropertiesv1 Schema</span></span>](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





