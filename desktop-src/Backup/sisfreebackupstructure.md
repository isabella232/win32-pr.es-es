---
title: Función SisFreeBackupStructure (Sisbkup. h)
description: Libera la estructura de copia de seguridad de SIS especificada.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Copia de seguridad de la función SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801670"
---
# <a name="sisfreebackupstructure-function"></a><span data-ttu-id="2f212-104">SisFreeBackupStructure función)</span><span class="sxs-lookup"><span data-stu-id="2f212-104">SisFreeBackupStructure function</span></span>

<span data-ttu-id="2f212-105">La función **SisFreeBackupStructure** libera la estructura de copia de seguridad de SIS especificada.</span><span class="sxs-lookup"><span data-stu-id="2f212-105">The **SisFreeBackupStructure** function frees the specified SIS backup structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f212-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f212-106">Syntax</span></span>


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a><span data-ttu-id="2f212-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f212-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f212-108">*sisBackupStructure* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f212-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f212-109">Puntero a la estructura de copia de seguridad de SIS devuelta desde [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="2f212-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f212-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f212-110">Return value</span></span>

<span data-ttu-id="2f212-111">Esta función devuelve **true** si se completa correctamente y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2f212-111">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="2f212-112">Llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información sobre la razón por la que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="2f212-112">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f212-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f212-113">Remarks</span></span>

<span data-ttu-id="2f212-114">Se debe llamar a esta función después de que se complete la operación de copia de seguridad para el volumen identificado por el valor del parámetro *sisBackupStructure* .</span><span class="sxs-lookup"><span data-stu-id="2f212-114">This function should be called after the backup operation is completed for the volume identified by the value of the *sisBackupStructure* parameter.</span></span>

<span data-ttu-id="2f212-115">Tenga en cuenta que no es seguro asumir que esto solo desasigna memoria.</span><span class="sxs-lookup"><span data-stu-id="2f212-115">Note that it is not safe to assume that this only deallocates memory.</span></span> <span data-ttu-id="2f212-116">Por ejemplo, esta función también puede realizar operaciones administrativas adicionales para la arquitectura de SIS.</span><span class="sxs-lookup"><span data-stu-id="2f212-116">For example, this function may also perform additional administrative operations for the SIS architecture.</span></span> <span data-ttu-id="2f212-117">Por lo tanto, llame a esta función incluso si la operación de copia de seguridad se cerrará inmediatamente después.</span><span class="sxs-lookup"><span data-stu-id="2f212-117">Therefore, call this function even if your backup operation will exit immediately afterward.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f212-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f212-118">Requirements</span></span>



| <span data-ttu-id="2f212-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f212-119">Requirement</span></span> | <span data-ttu-id="2f212-120">Value</span><span class="sxs-lookup"><span data-stu-id="2f212-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f212-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f212-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2f212-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2f212-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2f212-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f212-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2f212-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f212-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2f212-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f212-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f212-126"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f212-126"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f212-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f212-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f212-128"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f212-128"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f212-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f212-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f212-130"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f212-130"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f212-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f212-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f212-132">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="2f212-132">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

