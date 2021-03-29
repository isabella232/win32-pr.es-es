---
title: Función SisFreeRestoreStructure (Sisbkup. h)
description: Libera la memoria asignada para la estructura de restauración de SIS especificada y realiza tareas que preparan el filtro SIS para configurar correctamente los vínculos creados durante la operación de restauración.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Copia de seguridad de la función SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492622"
---
# <a name="sisfreerestorestructure-function"></a><span data-ttu-id="a6d32-104">SisFreeRestoreStructure función)</span><span class="sxs-lookup"><span data-stu-id="a6d32-104">SisFreeRestoreStructure function</span></span>

<span data-ttu-id="a6d32-105">La función **SisFreeRestoreStructure** libera la memoria asignada para la estructura de restauración de SIS especificada y realiza tareas que preparan el filtro SIS para configurar correctamente los vínculos creados durante la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="a6d32-105">The **SisFreeRestoreStructure** function frees the memory allocated for the specified SIS restore structure, and performs tasks that prepare the SIS filter to properly set up the links created during the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d32-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6d32-106">Syntax</span></span>


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a><span data-ttu-id="a6d32-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6d32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6d32-108">*sisRestoreStructure* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6d32-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6d32-109">Puntero a una estructura de restauración de SIS devuelta desde [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="a6d32-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6d32-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6d32-110">Return value</span></span>

<span data-ttu-id="a6d32-111">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a6d32-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="a6d32-112">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6d32-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d32-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6d32-113">Remarks</span></span>

<span data-ttu-id="a6d32-114">El acceso a los vínculos de SIS antes de que se complete la llamada a esta función puede producir una comprobación de volumen o una lectura parcial del contenido del vínculo.</span><span class="sxs-lookup"><span data-stu-id="a6d32-114">Accessing the SIS links before the call to this function completes can result in a volume check or a partial read of the link's contents.</span></span>

<span data-ttu-id="a6d32-115">Tenga en cuenta que no es seguro asumir que esto solo desasigna memoria.</span><span class="sxs-lookup"><span data-stu-id="a6d32-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="a6d32-116">Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS.</span><span class="sxs-lookup"><span data-stu-id="a6d32-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="a6d32-117">Por lo tanto, llame a esta función incluso si la operación de restauración se cerrará inmediatamente después.</span><span class="sxs-lookup"><span data-stu-id="a6d32-117">Therefore, call this function even if your restore operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6d32-118">Requirements</span></span>



| <span data-ttu-id="a6d32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6d32-119">Requirement</span></span> | <span data-ttu-id="a6d32-120">Value</span><span class="sxs-lookup"><span data-stu-id="a6d32-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d32-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6d32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d32-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a6d32-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a6d32-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6d32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d32-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6d32-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a6d32-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6d32-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6d32-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6d32-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6d32-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6d32-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6d32-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6d32-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="a6d32-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6d32-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6d32-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6d32-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6d32-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6d32-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d32-132">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="a6d32-132">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> </dl>

 

