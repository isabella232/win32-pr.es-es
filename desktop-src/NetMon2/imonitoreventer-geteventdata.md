---
description: El método GetEventData asigna espacio para las estructuras NMEVENTDATA y NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'IMonitorEventer:: GetEventData (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275338"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="d7f8e-103">IMonitorEventer:: GetEventData (método)</span><span class="sxs-lookup"><span data-stu-id="d7f8e-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="d7f8e-104">El método **GetEventData** asigna espacio para las estructuras [NMEVENTDATA](nmeventdata.md) y [NMCOLUMNINFO](nmcolumninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d7f8e-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f8e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7f8e-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="d7f8e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7f8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f8e-107">*bNumColumns* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7f8e-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8e-108">Número de estructuras **NMCOLUMNINFO** necesarias.</span><span class="sxs-lookup"><span data-stu-id="d7f8e-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="d7f8e-109">*ppNMEventData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7f8e-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f8e-110">Dirección de la estructura **NMEVENTDATA** que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="d7f8e-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f8e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7f8e-111">Return value</span></span>

<span data-ttu-id="d7f8e-112">Si el método se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7f8e-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="d7f8e-113">Si el método no se realiza correctamente, el valor devuelto es \_ NMERR \_ de \_ memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="d7f8e-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f8e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7f8e-114">Remarks</span></span>

<span data-ttu-id="d7f8e-115">Los monitores llaman a este método para asignar memoria para los datos de evento y las estructuras de información de columnas.</span><span class="sxs-lookup"><span data-stu-id="d7f8e-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="d7f8e-116">Para liberar memoria asignada para una estructura **NMEVENTDATA** , vea [IMonitorEventer:: FreeEventData](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="d7f8e-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f8e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f8e-117">Requirements</span></span>



| <span data-ttu-id="d7f8e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f8e-118">Requirement</span></span> | <span data-ttu-id="d7f8e-119">Value</span><span class="sxs-lookup"><span data-stu-id="d7f8e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f8e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f8e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f8e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7f8e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7f8e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f8e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f8e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7f8e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7f8e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7f8e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f8e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f8e-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f8e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f8e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f8e-127">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="d7f8e-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="d7f8e-128">IMonitorEventer::FreeEventData</span><span class="sxs-lookup"><span data-stu-id="d7f8e-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="d7f8e-129">NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="d7f8e-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="d7f8e-130">NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="d7f8e-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




