---
description: Cierra la base de datos especificada.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: SdbCloseDatabaseWrite función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907158"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="de9e6-103">SdbCloseDatabaseWrite función)</span><span class="sxs-lookup"><span data-stu-id="de9e6-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="de9e6-104">Cierra la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="de9e6-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de9e6-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="de9e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de9e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9e6-107">archivo *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de9e6-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de9e6-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="de9e6-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9e6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de9e6-109">Return value</span></span>

<span data-ttu-id="de9e6-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="de9e6-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9e6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de9e6-111">Remarks</span></span>

<span data-ttu-id="de9e6-112">Esta función llama a [**SdbCloseDatabase**](sdbclosedatabase.md); por lo tanto, estas dos funciones son equivalentes.</span><span class="sxs-lookup"><span data-stu-id="de9e6-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9e6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9e6-113">Requirements</span></span>



| <span data-ttu-id="de9e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9e6-114">Requirement</span></span> | <span data-ttu-id="de9e6-115">Value</span><span class="sxs-lookup"><span data-stu-id="de9e6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de9e6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de9e6-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="de9e6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de9e6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de9e6-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="de9e6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="de9e6-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de9e6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de9e6-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de9e6-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9e6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="de9e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9e6-123">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="de9e6-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="de9e6-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="de9e6-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="de9e6-125">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="de9e6-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




