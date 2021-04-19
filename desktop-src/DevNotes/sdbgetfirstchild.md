---
description: Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del primer elemento secundario.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538254"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="9e94e-103">SdbGetFirstChild función)</span><span class="sxs-lookup"><span data-stu-id="9e94e-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="9e94e-104">Busca una etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del primer elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="9e94e-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e94e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e94e-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="9e94e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e94e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e94e-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e94e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e94e-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="9e94e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="9e94e-109">*tiParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9e94e-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e94e-110">El **TAGID** del inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9e94e-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="9e94e-111">Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="9e94e-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e94e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e94e-112">Return value</span></span>

<span data-ttu-id="9e94e-113">El valor de **TagID** del primer elemento secundario o **TagID \_ null** no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="9e94e-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e94e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e94e-114">Requirements</span></span>



| <span data-ttu-id="9e94e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e94e-115">Requirement</span></span> | <span data-ttu-id="9e94e-116">Value</span><span class="sxs-lookup"><span data-stu-id="9e94e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e94e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e94e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e94e-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9e94e-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9e94e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e94e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e94e-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e94e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e94e-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e94e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e94e-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e94e-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e94e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e94e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e94e-124">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="9e94e-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="9e94e-125">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="9e94e-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="9e94e-126">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="9e94e-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




