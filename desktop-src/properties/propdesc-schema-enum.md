---
description: Se usa para asignar texto enumerado a valores discretos.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b615697e669f8d02e0530a1763309cfe74113467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667495"
---
# <a name="enum"></a><span data-ttu-id="80073-103">enum</span><span class="sxs-lookup"><span data-stu-id="80073-103">enum</span></span>

<span data-ttu-id="80073-104">Se usa para asignar texto enumerado a valores discretos.</span><span class="sxs-lookup"><span data-stu-id="80073-104">Used to assign enumerated text to discrete values.</span></span> <span data-ttu-id="80073-105">Puede haber cualquier número de estos elementos en un [enumeratedList](./propdesc-schema-enumeratedlist.md).</span><span class="sxs-lookup"><span data-stu-id="80073-105">Any number of these elements may exist under an [enumeratedList](./propdesc-schema-enumeratedlist.md).</span></span> <span data-ttu-id="80073-106">Mediante programación, se representan como objetos IPropertyEnumType, cuyo método [**IPropertyEnumType:: GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) devuelve PET \_ DISCRETEVALUE.</span><span class="sxs-lookup"><span data-stu-id="80073-106">Programmatically, these are represented as IPropertyEnumType objects, whose [**IPropertyEnumType::GetEnumType**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) method returns PET\_DISCRETEVALUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="80073-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80073-107">Syntax</span></span>


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="80073-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="80073-108">Element Information</span></span>



| <span data-ttu-id="80073-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="80073-109">Parent Element</span></span>                                         | <span data-ttu-id="80073-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="80073-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="80073-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="80073-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="80073-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="80073-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="80073-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="80073-113">Attributes</span></span>



| <span data-ttu-id="80073-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="80073-114">Attribute</span></span> | <span data-ttu-id="80073-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="80073-115">Description</span></span>                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80073-116">value</span><span class="sxs-lookup"><span data-stu-id="80073-116">value</span></span>     | <span data-ttu-id="80073-117">Público.</span><span class="sxs-lookup"><span data-stu-id="80073-117">Public.</span></span> <span data-ttu-id="80073-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="80073-118">Required.</span></span> <span data-ttu-id="80073-119">Valor discreto (cadena o número) al que se va a asignar el texto enumerado.</span><span class="sxs-lookup"><span data-stu-id="80073-119">The discrete value (string or number) to be assigned enumerated text to.</span></span>                                                                                                                           |
| <span data-ttu-id="80073-120">text</span><span class="sxs-lookup"><span data-stu-id="80073-120">text</span></span>      | <span data-ttu-id="80073-121">Público.</span><span class="sxs-lookup"><span data-stu-id="80073-121">Public.</span></span> <span data-ttu-id="80073-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="80073-122">Required.</span></span> <span data-ttu-id="80073-123">Texto que se usa para mostrar el valor enumerado.</span><span class="sxs-lookup"><span data-stu-id="80073-123">The text used to display the enumerated value.</span></span> <span data-ttu-id="80073-124">La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; Utilice la cadena de presentación indirecta para que se pueda localizar.</span><span class="sxs-lookup"><span data-stu-id="80073-124">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span> |
| <span data-ttu-id="80073-125">teclas de acceso</span><span class="sxs-lookup"><span data-stu-id="80073-125">mnemonics</span></span> | <span data-ttu-id="80073-126">**Windows 7 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="80073-126">**Windows 7 and later.**</span></span> <span data-ttu-id="80073-127">Público.</span><span class="sxs-lookup"><span data-stu-id="80073-127">Public.</span></span> <span data-ttu-id="80073-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="80073-128">Optional.</span></span> <span data-ttu-id="80073-129">Una lista de valores de tecla de tecla que se pueden usar para hacer referencia a la propiedad en consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="80073-129">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="80073-130">La lista está delimitada por el \| carácter ' '.</span><span class="sxs-lookup"><span data-stu-id="80073-130">The list is delimited with the '\|' character.</span></span>                                     |



 

 

 
