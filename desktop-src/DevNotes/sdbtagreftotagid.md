---
description: Recupera el TAGID y un identificador de la base de datos de Shim para el TAGREF especificado.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: SdbTagRefToTagID función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152958"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="ab6f3-103">SdbTagRefToTagID función)</span><span class="sxs-lookup"><span data-stu-id="ab6f3-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="ab6f3-104">Recupera el **TAGID** y un identificador de la base de datos de Shim para el [**TAGREF**](tagref.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6f3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab6f3-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="ab6f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab6f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6f3-107">*hSDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-108">Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="ab6f3-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-109">*trWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-110">[**TAGREF**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="ab6f3-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-111">*ppdb* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-112">El identificador resultante para la base de datos de Shim.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ab6f3-113">*ptiWhich* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6f3-114">El **TAGID** resultante.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6f3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab6f3-115">Return value</span></span>

<span data-ttu-id="ab6f3-116">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6f3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab6f3-117">Requirements</span></span>



| <span data-ttu-id="ab6f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6f3-118">Requirement</span></span> | <span data-ttu-id="ab6f3-119">Value</span><span class="sxs-lookup"><span data-stu-id="ab6f3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6f3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab6f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6f3-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ab6f3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab6f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6f3-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab6f3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ab6f3-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab6f3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab6f3-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f3-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6f3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab6f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6f3-127">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="ab6f3-128">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="ab6f3-129">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




