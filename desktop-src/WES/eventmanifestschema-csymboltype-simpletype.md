---
title: Tipo simple CSymbolType (registro de eventos de Windows)
description: Define un nombre de símbolo de C/C++ válido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- CSymbolType de tipo simple de registro
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695925"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="ee2da-104">Tipo simple CSymbolType (registro de eventos de Windows)</span><span class="sxs-lookup"><span data-stu-id="ee2da-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="ee2da-105">Define un nombre de símbolo de C/C++ válido.</span><span class="sxs-lookup"><span data-stu-id="ee2da-105">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="ee2da-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="ee2da-106">Patterns</span></span>

<span data-ttu-id="ee2da-107">El tipo simple **CSymbolType** es **xs: String** , que está restringido por el patrón siguiente:</span><span class="sxs-lookup"><span data-stu-id="ee2da-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="ee2da-108">El nombre del símbolo puede estar vacío o contener caracteres alfanuméricos y caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="ee2da-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="ee2da-109">Si el nombre está vacío, el compilador de mensajes generará el nombre del símbolo.</span><span class="sxs-lookup"><span data-stu-id="ee2da-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="ee2da-110">Si especifica un nombre, el nombre debe comenzar con un carácter de subrayado ( \_ ) o alfabético.</span><span class="sxs-lookup"><span data-stu-id="ee2da-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee2da-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee2da-111">Remarks</span></span>

<span data-ttu-id="ee2da-112">Si el nombre del símbolo está vacío, el compilador de mensajes utiliza el atributo de **nombre** del elemento que está definiendo para generar el nombre del símbolo.</span><span class="sxs-lookup"><span data-stu-id="ee2da-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="ee2da-113">El compilador reemplaza los caracteres no alfanuméricos y los dígitos iniciales por caracteres de subrayado.</span><span class="sxs-lookup"><span data-stu-id="ee2da-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="ee2da-114">Por ejemplo, si el atributo de **nombre** del canal es Microsoft-Windows-SampleProvider/Operational, el compilador usaría Microsoft \_ Windows \_ SampleProvider \_ Operational como el nombre del símbolo.</span><span class="sxs-lookup"><span data-stu-id="ee2da-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2da-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2da-115">Requirements</span></span>



| <span data-ttu-id="ee2da-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2da-116">Requirement</span></span> | <span data-ttu-id="ee2da-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee2da-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ee2da-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2da-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2da-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2da-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ee2da-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2da-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2da-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2da-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





