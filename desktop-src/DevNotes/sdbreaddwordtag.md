---
Description: Recupera el valor DWORD para el TAGID especificado.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151035"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="b5791-103">SdbReadDWORDTag función)</span><span class="sxs-lookup"><span data-stu-id="b5791-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="b5791-104">Recupera el valor **DWORD** para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="b5791-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5791-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5791-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="b5791-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5791-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5791-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5791-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="b5791-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="b5791-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5791-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5791-110">**TAGID** que corresponde a los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b5791-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b5791-111">*dwDefault* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5791-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5791-112">El valor predeterminado que se devolverá en caso de error.</span><span class="sxs-lookup"><span data-stu-id="b5791-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5791-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5791-113">Return value</span></span>

<span data-ttu-id="b5791-114">La función devuelve el valor si se ejecuta correctamente o *dwDefault* en caso de error.</span><span class="sxs-lookup"><span data-stu-id="b5791-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5791-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5791-115">Requirements</span></span>



| <span data-ttu-id="b5791-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5791-116">Requirement</span></span> | <span data-ttu-id="b5791-117">Value</span><span class="sxs-lookup"><span data-stu-id="b5791-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5791-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5791-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5791-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b5791-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b5791-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5791-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5791-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5791-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5791-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5791-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5791-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5791-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5791-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5791-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5791-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="b5791-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="b5791-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="b5791-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="b5791-127">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="b5791-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="b5791-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="b5791-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




