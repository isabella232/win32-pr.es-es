---
description: .
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: Elemento Image (esquema de descripción de propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb519d5f8104d114734e1f12676f213312e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666862"
---
# <a name="image"></a><span data-ttu-id="c583a-103">imagen</span><span class="sxs-lookup"><span data-stu-id="c583a-103">image</span></span>

<span data-ttu-id="c583a-104">Solo debe haber un elemento de [imagen]() para cada elemento primario.</span><span class="sxs-lookup"><span data-stu-id="c583a-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c583a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c583a-105">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c583a-106">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="c583a-106">Element Information</span></span>



| <span data-ttu-id="c583a-107">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="c583a-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="c583a-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c583a-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="c583a-109">[enumeración](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="c583a-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="c583a-110">None</span><span class="sxs-lookup"><span data-stu-id="c583a-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="c583a-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="c583a-111">Attributes</span></span>



| <span data-ttu-id="c583a-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="c583a-112">Attribute</span></span> | <span data-ttu-id="c583a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c583a-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="c583a-114">res</span><span class="sxs-lookup"><span data-stu-id="c583a-114">res</span></span>       | <span data-ttu-id="c583a-115">Público.</span><span class="sxs-lookup"><span data-stu-id="c583a-115">Public.</span></span> <span data-ttu-id="c583a-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c583a-116">Required.</span></span> |



 

 

 
