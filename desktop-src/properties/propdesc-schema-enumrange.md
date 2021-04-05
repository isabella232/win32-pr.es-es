---
description: Asigna texto de enumeración a un intervalo de valores. Cada elemento enumRange especifica un valor mínimo y se extiende hasta el valor mínimo del elemento siguiente, o hasta que no hay más elementos enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001573"
---
# <a name="enumrange"></a><span data-ttu-id="cccc4-104">enumRange</span><span class="sxs-lookup"><span data-stu-id="cccc4-104">enumRange</span></span>

<span data-ttu-id="cccc4-105">Asigna texto de enumeración a un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="cccc4-105">Assigns enumeration text to a range of values.</span></span> <span data-ttu-id="cccc4-106">Cada elemento [enumRange]() especifica un valor mínimo y se extiende hasta el valor mínimo del elemento siguiente, o hasta que no hay más elementos enumRange.</span><span class="sxs-lookup"><span data-stu-id="cccc4-106">Each [enumRange]() element specifies a minimum value, and extends until the next element minimum value, or until there are no more enumRange elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="cccc4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cccc4-107">Syntax</span></span>

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="cccc4-108">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="cccc4-108">Element Information</span></span>



| <span data-ttu-id="cccc4-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="cccc4-109">Parent Element</span></span>                                         | <span data-ttu-id="cccc4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cccc4-110">Child Elements</span></span> |
|--------------------------------------------------------|----------------|
| [<span data-ttu-id="cccc4-111">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="cccc4-111">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md) | <span data-ttu-id="cccc4-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="cccc4-112">none</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="cccc4-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="cccc4-113">Attributes</span></span>



| <span data-ttu-id="cccc4-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="cccc4-114">Attribute</span></span> | <span data-ttu-id="cccc4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="cccc4-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cccc4-116">minValue</span><span class="sxs-lookup"><span data-stu-id="cccc4-116">minValue</span></span>  | <span data-ttu-id="cccc4-117">Público.</span><span class="sxs-lookup"><span data-stu-id="cccc4-117">Public.</span></span> <span data-ttu-id="cccc4-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cccc4-118">Required.</span></span> <span data-ttu-id="cccc4-119">Valor mínimo del intervalo.</span><span class="sxs-lookup"><span data-stu-id="cccc4-119">The minimum value in the range.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cccc4-120">setValue</span><span class="sxs-lookup"><span data-stu-id="cccc4-120">setValue</span></span>  | <span data-ttu-id="cccc4-121">Público.</span><span class="sxs-lookup"><span data-stu-id="cccc4-121">Public.</span></span> <span data-ttu-id="cccc4-122">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cccc4-122">Optional.</span></span> <span data-ttu-id="cccc4-123">Cuando un usuario selecciona esta enumeración desde un control de propiedad ListBox, este valor discreto se asigna como el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="cccc4-123">When a user selects this enumeration from a listbox property control, this discrete value is assigned as the property value.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cccc4-124">text</span><span class="sxs-lookup"><span data-stu-id="cccc4-124">text</span></span>      | <span data-ttu-id="cccc4-125">Público.</span><span class="sxs-lookup"><span data-stu-id="cccc4-125">Public.</span></span> <span data-ttu-id="cccc4-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cccc4-126">Optional.</span></span> <span data-ttu-id="cccc4-127">Texto que se usa para mostrar el valor enumerado.</span><span class="sxs-lookup"><span data-stu-id="cccc4-127">The text used to display the enumerated value.</span></span> <span data-ttu-id="cccc4-128">La sintaxis permite una cadena de presentación directa o una referencia de cadena de presentación indirecta; Utilice la cadena de presentación indirecta para que se pueda localizar.</span><span class="sxs-lookup"><span data-stu-id="cccc4-128">The syntax allows for a direct display string or an indirect display string reference; use the indirect display string so that it can be localized.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cccc4-129">teclas de acceso</span><span class="sxs-lookup"><span data-stu-id="cccc4-129">mnemonics</span></span> | <span data-ttu-id="cccc4-130">**Windows 7 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="cccc4-130">**Windows 7 and later.**</span></span> <span data-ttu-id="cccc4-131">Público.</span><span class="sxs-lookup"><span data-stu-id="cccc4-131">Public.</span></span> <span data-ttu-id="cccc4-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cccc4-132">Optional.</span></span> <span data-ttu-id="cccc4-133">Una lista de valores de tecla de tecla que se pueden usar para hacer referencia a la propiedad en consultas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cccc4-133">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="cccc4-134">La lista está delimitada por el \| carácter ' '.</span><span class="sxs-lookup"><span data-stu-id="cccc4-134">The list is delimited with the '\|' character.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cccc4-135">name</span><span class="sxs-lookup"><span data-stu-id="cccc4-135">name</span></span>      | <span data-ttu-id="cccc4-136">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cccc4-136">Required.</span></span> <span data-ttu-id="cccc4-137">Nombre canónico de la propiedad, único para el sistema; por ejemplo, System. Rating.</span><span class="sxs-lookup"><span data-stu-id="cccc4-137">The canonical property name, unique to the system; for example, System.Rating.</span></span> <span data-ttu-id="cccc4-138">Este atributo está limitado a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cccc4-138">This attribute is limited to 64 characters.</span></span> <span data-ttu-id="cccc4-139">El nombre distingue mayúsculas de minúsculas y debe usar la sintaxis siguiente: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="cccc4-139">The name is case sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="cccc4-140">Los métodos siguientes devuelven este valor: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)y [**IPropertyUI:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cccc4-140">The following methods return this value: [**IExplorerCommand::GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2::GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2), and [**IPropertyUI::GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)).</span></span> |



 

 

 
