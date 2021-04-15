---
Description: Recupera el valor QWORD para el TAGID especificado.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422583"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="63e15-103">SdbReadQWORDTag función)</span><span class="sxs-lookup"><span data-stu-id="63e15-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="63e15-104">Recupera el valor **QWord** para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="63e15-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e15-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="63e15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63e15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e15-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e15-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e15-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="63e15-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="63e15-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e15-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e15-110">**TAGID** que corresponde a los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="63e15-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="63e15-111">*qwDefault* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e15-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e15-112">El valor predeterminado que se devolverá en caso de error.</span><span class="sxs-lookup"><span data-stu-id="63e15-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e15-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63e15-113">Return value</span></span>

<span data-ttu-id="63e15-114">La función devuelve el valor si se ejecuta correctamente o *qwDefault* en caso de error.</span><span class="sxs-lookup"><span data-stu-id="63e15-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e15-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e15-115">Requirements</span></span>



| <span data-ttu-id="63e15-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e15-116">Requirement</span></span> | <span data-ttu-id="63e15-117">Value</span><span class="sxs-lookup"><span data-stu-id="63e15-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e15-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63e15-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="63e15-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="63e15-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63e15-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63e15-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63e15-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63e15-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e15-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e15-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e15-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e15-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e15-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="63e15-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="63e15-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="63e15-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="63e15-127">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="63e15-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="63e15-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="63e15-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




