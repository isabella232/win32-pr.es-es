---
description: Cierra la base de datos de Shim especificada.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: SdbCloseDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080185"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="63871-103">SdbCloseDatabase función)</span><span class="sxs-lookup"><span data-stu-id="63871-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="63871-104">Cierra la base de datos de Shim especificada.</span><span class="sxs-lookup"><span data-stu-id="63871-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="63871-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63871-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="63871-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63871-107">archivo *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="63871-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63871-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="63871-108">A handle to the shim database.</span></span> <span data-ttu-id="63871-109">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="63871-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63871-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63871-110">Return value</span></span>

<span data-ttu-id="63871-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63871-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="63871-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63871-112">Requirements</span></span>



| <span data-ttu-id="63871-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="63871-113">Requirement</span></span> | <span data-ttu-id="63871-114">Value</span><span class="sxs-lookup"><span data-stu-id="63871-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63871-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63871-115">Minimum supported client</span></span><br/> | <span data-ttu-id="63871-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63871-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="63871-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63871-117">Minimum supported server</span></span><br/> | <span data-ttu-id="63871-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63871-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63871-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63871-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63871-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63871-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63871-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="63871-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63871-122">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="63871-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




