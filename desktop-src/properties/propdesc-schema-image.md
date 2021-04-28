---
description: imagen
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: elemento image (esquema de descripción de propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104993"
---
# <a name="image"></a><span data-ttu-id="ee87d-103">imagen</span><span class="sxs-lookup"><span data-stu-id="ee87d-103">image</span></span>

<span data-ttu-id="ee87d-104">Solo debe haber un elemento [image]() para cada elemento primario.</span><span class="sxs-lookup"><span data-stu-id="ee87d-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee87d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee87d-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="ee87d-106">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ee87d-106">Element Information</span></span>



| <span data-ttu-id="ee87d-107">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ee87d-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="ee87d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee87d-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="ee87d-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="ee87d-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="ee87d-110">None</span><span class="sxs-lookup"><span data-stu-id="ee87d-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="ee87d-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ee87d-111">Attributes</span></span>



| <span data-ttu-id="ee87d-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="ee87d-112">Attribute</span></span> | <span data-ttu-id="ee87d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee87d-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="ee87d-114">res</span><span class="sxs-lookup"><span data-stu-id="ee87d-114">res</span></span>       | <span data-ttu-id="ee87d-115">Público.</span><span class="sxs-lookup"><span data-stu-id="ee87d-115">Public.</span></span> <span data-ttu-id="ee87d-116">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ee87d-116">Required.</span></span> |



 

 

 
