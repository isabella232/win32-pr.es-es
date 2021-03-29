---
description: Se produce cuando hay un evento del sistema disponible.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'ITabletEventSink:: SystemEvent (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648509"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="3b8ba-103">ITabletEventSink:: SystemEvent (método)</span><span class="sxs-lookup"><span data-stu-id="3b8ba-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="3b8ba-104">Se produce cuando hay un evento del sistema disponible.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b8ba-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="3b8ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b8ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b8ba-107">*TCID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b8ba-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8ba-108">El identificador de la tableta.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="3b8ba-109">*CID* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="3b8ba-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8ba-110">Identificador del lápiz óptico.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="3b8ba-111">*evento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3b8ba-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8ba-112">Código de evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="3b8ba-113">*EventData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b8ba-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b8ba-114">Datos de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b8ba-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b8ba-115">Return value</span></span>

<span data-ttu-id="3b8ba-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-116">This method can return one of these values.</span></span>



| <span data-ttu-id="3b8ba-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3b8ba-117">Return code</span></span>                                                                            | <span data-ttu-id="3b8ba-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b8ba-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3b8ba-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ba-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3b8ba-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3b8ba-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ba-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3b8ba-122">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b8ba-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b8ba-123">Remarks</span></span>

<span data-ttu-id="3b8ba-124">La lista siguiente contiene los valores válidos para el parámetro de evento.</span><span class="sxs-lookup"><span data-stu-id="3b8ba-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="3b8ba-125">SE \_ TAP</span><span class="sxs-lookup"><span data-stu-id="3b8ba-125">SE\_TAP</span></span>
-   <span data-ttu-id="3b8ba-126">SE \_ \_ TAP doble</span><span class="sxs-lookup"><span data-stu-id="3b8ba-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="3b8ba-127">SE \_ \_ TAP derecho</span><span class="sxs-lookup"><span data-stu-id="3b8ba-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="3b8ba-128">SE ha \_ arrastrado</span><span class="sxs-lookup"><span data-stu-id="3b8ba-128">SE\_DRAG</span></span>
-   <span data-ttu-id="3b8ba-129">SE \_ arrastra a la derecha \_</span><span class="sxs-lookup"><span data-stu-id="3b8ba-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="3b8ba-130">SE \_ mantiene presionado \_ entrar</span><span class="sxs-lookup"><span data-stu-id="3b8ba-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="3b8ba-131">SE \_ mantiene presionado \_</span><span class="sxs-lookup"><span data-stu-id="3b8ba-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="3b8ba-132">SE \_ mantiene el mouse \_ Enter</span><span class="sxs-lookup"><span data-stu-id="3b8ba-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="3b8ba-133">mantener el \_ mouse en \_ salir</span><span class="sxs-lookup"><span data-stu-id="3b8ba-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="3b8ba-134">SE \_ hace clic con el botón \_</span><span class="sxs-lookup"><span data-stu-id="3b8ba-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="3b8ba-135">\_tecla se</span><span class="sxs-lookup"><span data-stu-id="3b8ba-135">SE\_KEY</span></span>
-   <span data-ttu-id="3b8ba-136">\_tecla modificador \_ se</span><span class="sxs-lookup"><span data-stu-id="3b8ba-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="3b8ba-137">\_modo de gestos de se \_</span><span class="sxs-lookup"><span data-stu-id="3b8ba-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="3b8ba-138">\_cursor se</span><span class="sxs-lookup"><span data-stu-id="3b8ba-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8ba-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b8ba-139">Requirements</span></span>



| <span data-ttu-id="3b8ba-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8ba-140">Requirement</span></span> | <span data-ttu-id="3b8ba-141">Value</span><span class="sxs-lookup"><span data-stu-id="3b8ba-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8ba-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b8ba-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8ba-143">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b8ba-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b8ba-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b8ba-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8ba-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b8ba-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3b8ba-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b8ba-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b8ba-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ba-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8ba-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b8ba-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8ba-149">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="3b8ba-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




