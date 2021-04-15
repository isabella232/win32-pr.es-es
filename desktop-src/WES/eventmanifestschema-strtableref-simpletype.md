---
title: Tipo simple de strTableRef
description: Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas del manifiesto o en un archivo de mensajes (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef de tipo simple de registro
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534384"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="d1b34-104">Tipo simple de strTableRef</span><span class="sxs-lookup"><span data-stu-id="d1b34-104">strTableRef Simple Type</span></span>

<span data-ttu-id="d1b34-105">Define una cadena que hace referencia a una cadena de mensaje que se define en una tabla de cadenas del manifiesto o en un archivo de mensajes (. MC).</span><span class="sxs-lookup"><span data-stu-id="d1b34-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="d1b34-106">Patrones</span><span class="sxs-lookup"><span data-stu-id="d1b34-106">Patterns</span></span>

<span data-ttu-id="d1b34-107">El tipo simple **strTableRef** es **xs: String** , que está restringido por el patrón siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1b34-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="d1b34-108">La cadena debe tener el formato $string. *stringid* o $MC.*symbolid*.</span><span class="sxs-lookup"><span data-stu-id="d1b34-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="d1b34-109">Si la cadena tiene el formato, $string. *stringid*, debe hacer referencia a una cadena en la sección [**stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d1b34-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="d1b34-110">Si la cadena tiene el formato, $mc.*symbolid*, debe hacer referencia a un símbolo definido en el archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1b34-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b34-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b34-111">Requirements</span></span>



| <span data-ttu-id="d1b34-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b34-112">Requirement</span></span> | <span data-ttu-id="d1b34-113">Value</span><span class="sxs-lookup"><span data-stu-id="d1b34-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1b34-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b34-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b34-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1b34-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d1b34-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b34-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b34-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1b34-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





