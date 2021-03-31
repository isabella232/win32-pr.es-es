---
title: VERSION (instrucción)
description: Define la información de versión de un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menús de instrucciones de versión y otros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784048"
---
# <a name="version-statement"></a><span data-ttu-id="864aa-104">VERSION (instrucción)</span><span class="sxs-lookup"><span data-stu-id="864aa-104">VERSION statement</span></span>

<span data-ttu-id="864aa-105">Define la información de versión de un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="864aa-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="864aa-106">El valor *DWORD* especificado aparece con el recurso en el compilado. Archivo RES.</span><span class="sxs-lookup"><span data-stu-id="864aa-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="864aa-107">Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene importancia para el sistema.</span><span class="sxs-lookup"><span data-stu-id="864aa-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="864aa-108">La instrucción de la **versión** aparece antes del principio del cuerpo de una definición de recursos [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**stringtable**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="864aa-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="864aa-109">El valor especificado se aplica solo a ese recurso.</span><span class="sxs-lookup"><span data-stu-id="864aa-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="864aa-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="864aa-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="864aa-111">Valor **DWORD** definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="864aa-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="864aa-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="864aa-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="864aa-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="864aa-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="864aa-114">**SUS**</span><span class="sxs-lookup"><span data-stu-id="864aa-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="864aa-115">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="864aa-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="864aa-116">**MENU**</span><span class="sxs-lookup"><span data-stu-id="864aa-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="864aa-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="864aa-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="864aa-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="864aa-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




