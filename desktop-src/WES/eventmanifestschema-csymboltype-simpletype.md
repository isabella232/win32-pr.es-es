---
title: Tipo simple CSymbolType (registro de eventos de Windows)
description: 'Tipo simple CSymbolType (registro de eventos de Windows): define un nombre de símbolo de C/C++ válido.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Tipo simple EventLog de CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090623"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="55192-104">Tipo simple CSymbolType (registro de eventos de Windows)</span><span class="sxs-lookup"><span data-stu-id="55192-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="55192-105">Define un nombre de símbolo de C/C++ válido.</span><span class="sxs-lookup"><span data-stu-id="55192-105">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="55192-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="55192-106">Patterns</span></span>

<span data-ttu-id="55192-107">El **tipo simple CSymbolType** es **un xs:string** restringido por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="55192-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="55192-108">El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="55192-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="55192-109">Si el nombre está vacío, el compilador del mensaje generará el nombre del símbolo.</span><span class="sxs-lookup"><span data-stu-id="55192-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="55192-110">Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o un carácter alfabético.</span><span class="sxs-lookup"><span data-stu-id="55192-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="55192-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55192-111">Remarks</span></span>

<span data-ttu-id="55192-112">Si el nombre del símbolo está vacío, el compilador del mensaje usa el atributo **name** del elemento que se va a definir para generar el nombre del símbolo.</span><span class="sxs-lookup"><span data-stu-id="55192-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="55192-113">El compilador reemplaza los caracteres no alfanuméricos y los dígitos iniciales por caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="55192-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="55192-114">Por ejemplo, si el  atributo name del canal es Microsoft-Windows-SampleProvider/Operational, el compilador usaría Microsoft Windows SampleProvider Operational como \_ nombre del \_ \_ símbolo.</span><span class="sxs-lookup"><span data-stu-id="55192-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="55192-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55192-115">Requirements</span></span>



| <span data-ttu-id="55192-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="55192-116">Requirement</span></span> | <span data-ttu-id="55192-117">Valor</span><span class="sxs-lookup"><span data-stu-id="55192-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="55192-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55192-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55192-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="55192-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="55192-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55192-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55192-121">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="55192-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





