---
description: Recupera los datos binarios para el TAGID especificado.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666173"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="3b79e-103">SdbGetBinaryTagData función)</span><span class="sxs-lookup"><span data-stu-id="3b79e-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="3b79e-104">Recupera los datos binarios para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="3b79e-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b79e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b79e-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="3b79e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b79e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b79e-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b79e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b79e-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3b79e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3b79e-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b79e-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b79e-110">**TAGID** que corresponde a los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3b79e-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b79e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b79e-111">Return value</span></span>

<span data-ttu-id="3b79e-112">La función devuelve un puntero a los datos binarios o **null** si **TAGID** no es válido.</span><span class="sxs-lookup"><span data-stu-id="3b79e-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b79e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b79e-113">Requirements</span></span>



| <span data-ttu-id="3b79e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b79e-114">Requirement</span></span> | <span data-ttu-id="3b79e-115">Value</span><span class="sxs-lookup"><span data-stu-id="3b79e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b79e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b79e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b79e-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3b79e-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3b79e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b79e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b79e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b79e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b79e-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b79e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b79e-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b79e-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b79e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b79e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b79e-123">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="3b79e-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="3b79e-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3b79e-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="3b79e-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3b79e-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="3b79e-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="3b79e-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




