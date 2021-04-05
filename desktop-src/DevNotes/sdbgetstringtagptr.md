---
description: Recupera los datos de cadena para el TAGID especificado.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: SdbGetStringTagPtr función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000577"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="1c6f9-103">SdbGetStringTagPtr función)</span><span class="sxs-lookup"><span data-stu-id="1c6f9-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="1c6f9-104">Recupera los datos de cadena para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c6f9-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="1c6f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c6f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6f9-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c6f9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6f9-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f9-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c6f9-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6f9-110">**TAGID** que corresponde a los datos de cadena que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6f9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c6f9-111">Return value</span></span>

<span data-ttu-id="1c6f9-112">La función devuelve un puntero a los datos de cadena o **null** si **TAGID** no es válido o no es de tipo **Tag Type \_ \_ String** o **tag \_ Type \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6f9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c6f9-113">Requirements</span></span>



| <span data-ttu-id="1c6f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c6f9-114">Requirement</span></span> | <span data-ttu-id="1c6f9-115">Value</span><span class="sxs-lookup"><span data-stu-id="1c6f9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6f9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c6f9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6f9-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1c6f9-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1c6f9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c6f9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6f9-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c6f9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c6f9-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c6f9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c6f9-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c6f9-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6f9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c6f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6f9-123">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="1c6f9-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="1c6f9-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="1c6f9-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="1c6f9-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="1c6f9-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="1c6f9-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="1c6f9-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




