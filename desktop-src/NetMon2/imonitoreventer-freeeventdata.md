---
description: El método FreeEventData libera el espacio asignado para la estructura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'IMonitorEventer:: FreeEventData (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677273"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="90677-103">IMonitorEventer:: FreeEventData (método)</span><span class="sxs-lookup"><span data-stu-id="90677-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="90677-104">El método **FreeEventData** libera el espacio asignado para la estructura [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="90677-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="90677-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90677-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="90677-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90677-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90677-107">*pNMEventData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90677-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90677-108">Dirección de la estructura [**NMEVENTDATA**](nmeventdata.md) , cuya memoria se libera.</span><span class="sxs-lookup"><span data-stu-id="90677-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90677-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90677-109">Return value</span></span>

<span data-ttu-id="90677-110">Este método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="90677-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="90677-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90677-111">Remarks</span></span>

<span data-ttu-id="90677-112">Los monitores llaman a este método para liberar la memoria que asignan a la estructura de datos del evento.</span><span class="sxs-lookup"><span data-stu-id="90677-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="90677-113">Tenga en cuenta que mientras el monitor todavía tenga un puntero a cadenas en una estructura [**NMEVENTDATA**](nmeventdata.md) asignada, se debe liberar la memoria de estas cadenas antes de llamar al método **FreeEventData** .</span><span class="sxs-lookup"><span data-stu-id="90677-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="90677-114">Para obtener más información sobre cómo asignar memoria para una estructura [**NMEVENTDATA**](nmeventdata.md) , vea [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="90677-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90677-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90677-115">Requirements</span></span>



| <span data-ttu-id="90677-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="90677-116">Requirement</span></span> | <span data-ttu-id="90677-117">Value</span><span class="sxs-lookup"><span data-stu-id="90677-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90677-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90677-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90677-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90677-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="90677-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90677-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90677-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90677-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90677-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90677-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90677-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="90677-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90677-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="90677-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90677-125">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="90677-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="90677-126">**IMonitorEventer::GetEventData**</span><span class="sxs-lookup"><span data-stu-id="90677-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="90677-127">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="90677-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




