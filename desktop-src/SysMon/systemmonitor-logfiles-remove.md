---
title: LogFiles. Remove (método)
description: Quita la instancia de LogFileItem especificada de la colección.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Quitar método SysMon
- Remove (método) SysMon, logfiles (clase)
- Logfiles (clase) SysMon, Remove (método)
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803350"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="d1b51-106">LogFiles. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="d1b51-106">LogFiles.Remove method</span></span>

<span data-ttu-id="d1b51-107">Quita la instancia de [**LogFileItem**](logfileitem.md) especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="d1b51-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b51-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1b51-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="d1b51-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1b51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b51-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d1b51-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b51-111">Índice de entero del archivo de registro que se va a quitar de la colección.</span><span class="sxs-lookup"><span data-stu-id="d1b51-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="d1b51-112">El índice está basado en uno.</span><span class="sxs-lookup"><span data-stu-id="d1b51-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b51-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1b51-113">Return value</span></span>

<span data-ttu-id="d1b51-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d1b51-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b51-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1b51-115">Remarks</span></span>

<span data-ttu-id="d1b51-116">**Antes de Windows Vista:** No se pueden quitar archivos de registro de la [**colección de archivos de registro**](systemmonitor-logfiles.md) si el valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) está establecido en sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="d1b51-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b51-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b51-117">Requirements</span></span>



| <span data-ttu-id="d1b51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b51-118">Requirement</span></span> | <span data-ttu-id="d1b51-119">Value</span><span class="sxs-lookup"><span data-stu-id="d1b51-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b51-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b51-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1b51-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d1b51-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b51-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1b51-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1b51-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1b51-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b51-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d1b51-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b51-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1b51-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b51-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="d1b51-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="d1b51-128">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="d1b51-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="d1b51-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="d1b51-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





