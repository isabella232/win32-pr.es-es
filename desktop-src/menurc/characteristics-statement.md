---
title: Instrucción CHARACTERISTICS
description: Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menús de instrucciones de características y otros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076728"
---
# <a name="characteristics-statement"></a><span data-ttu-id="ca140-104">Instrucción CHARACTERISTICS</span><span class="sxs-lookup"><span data-stu-id="ca140-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="ca140-105">Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca140-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="ca140-106">El valor **DWORD** especificado aparece con el recurso en el archivo. res compilado.</span><span class="sxs-lookup"><span data-stu-id="ca140-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="ca140-107">Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene importancia para el sistema.</span><span class="sxs-lookup"><span data-stu-id="ca140-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="ca140-108">La instrucción **Characteristics** aparece antes del principio del cuerpo de un [**acelerador**](accelerators-resource.md), [**cuadro de diálogo**](dialog-resource.md), [**menú**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o definición de recursos [**stringtable**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="ca140-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="ca140-109">El valor especificado se aplica solo a ese recurso.</span><span class="sxs-lookup"><span data-stu-id="ca140-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="ca140-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="ca140-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="ca140-111">Valor **DWORD** definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ca140-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ca140-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca140-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca140-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="ca140-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="ca140-114">**DIÁLOGO**</span><span class="sxs-lookup"><span data-stu-id="ca140-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="ca140-115">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="ca140-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="ca140-116">**MENU**</span><span class="sxs-lookup"><span data-stu-id="ca140-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="ca140-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="ca140-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="ca140-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="ca140-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




