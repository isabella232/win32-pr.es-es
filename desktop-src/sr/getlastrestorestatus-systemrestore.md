---
title: Método GetLastRestoreStatus de la clase SystemRestore
description: Recupera el estado de la última restauración del sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Método GetLastRestoreStatus Restaurar sistema
- Método GetLastRestoreStatus Restaurar sistema, clase SystemRestore
- SystemRestore Class System Restore, GetLastRestoreStatus método
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705115"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="dfe45-106">Método GetLastRestoreStatus de la clase SystemRestore</span><span class="sxs-lookup"><span data-stu-id="dfe45-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="dfe45-107">Recupera el estado de la última restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="dfe45-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe45-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfe45-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="dfe45-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfe45-109">Parameters</span></span>

<span data-ttu-id="dfe45-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dfe45-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfe45-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfe45-111">Return value</span></span>

<span data-ttu-id="dfe45-112">El método devuelve uno de los siguientes valores de estado.</span><span class="sxs-lookup"><span data-stu-id="dfe45-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="dfe45-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfe45-113">Return value</span></span>                                                                 | <span data-ttu-id="dfe45-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfe45-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dfe45-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dfe45-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="dfe45-116">Error en la última restauración.</span><span class="sxs-lookup"><span data-stu-id="dfe45-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="dfe45-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dfe45-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="dfe45-118">La última restauración se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dfe45-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="dfe45-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dfe45-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dfe45-120">Se interrumpió la última restauración.</span><span class="sxs-lookup"><span data-stu-id="dfe45-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="dfe45-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfe45-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="dfe45-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfe45-122">Requirements</span></span>



| <span data-ttu-id="dfe45-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe45-123">Requirement</span></span> | <span data-ttu-id="dfe45-124">Value</span><span class="sxs-lookup"><span data-stu-id="dfe45-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dfe45-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe45-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe45-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dfe45-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dfe45-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfe45-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe45-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dfe45-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="dfe45-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dfe45-129">Namespace</span></span><br/>                | <span data-ttu-id="dfe45-130">Raíz \\ predeterminada</span><span class="sxs-lookup"><span data-stu-id="dfe45-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="dfe45-131">MOF</span><span class="sxs-lookup"><span data-stu-id="dfe45-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfe45-132"><dt>MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dfe45-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe45-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfe45-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe45-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="dfe45-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





