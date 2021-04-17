---
description: El método GetLocked recupera el estado de edición del objeto (bloqueado o desbloqueado).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'IAMTimelineObj:: GetLocked (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680850"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="f641c-103">IAMTimelineObj:: GetLocked (método)</span><span class="sxs-lookup"><span data-stu-id="f641c-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="f641c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f641c-104">\[Deprecated.</span></span> <span data-ttu-id="f641c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f641c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f641c-106">El `GetLocked` método recupera el estado de edición del objeto (bloqueado o desbloqueado).</span><span class="sxs-lookup"><span data-stu-id="f641c-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="f641c-107">Un estado bloqueado indica que el objeto no se debe editar; un estado desbloqueado indica que el objeto se puede editar.</span><span class="sxs-lookup"><span data-stu-id="f641c-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="f641c-108">La escala de tiempo no aplica el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f641c-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="f641c-109">La configuración bloqueada solo existe para la comodidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f641c-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="f641c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f641c-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f641c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f641c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f641c-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f641c-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f641c-113">Recibe el estado de edición del objeto.</span><span class="sxs-lookup"><span data-stu-id="f641c-113">Receives the object's editing state.</span></span> <span data-ttu-id="f641c-114">Si el valor es **true**, el objeto está bloqueado y no se debe editar.</span><span class="sxs-lookup"><span data-stu-id="f641c-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="f641c-115">Si es **false**, el objeto se desbloquea y se puede editar.</span><span class="sxs-lookup"><span data-stu-id="f641c-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f641c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f641c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f641c-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f641c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f641c-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f641c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f641c-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f641c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f641c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f641c-120">Requirements</span></span>



| <span data-ttu-id="f641c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f641c-121">Requirement</span></span> | <span data-ttu-id="f641c-122">Value</span><span class="sxs-lookup"><span data-stu-id="f641c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f641c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f641c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f641c-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f641c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f641c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f641c-125">Library</span></span><br/> | <dl> <span data-ttu-id="f641c-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f641c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f641c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f641c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f641c-128">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f641c-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f641c-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f641c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




