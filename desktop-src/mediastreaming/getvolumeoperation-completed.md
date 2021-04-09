---
title: Propiedad GetVolumeOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetVolumeAsync.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz GetVolumeOperation
- Interfaz GetVolumeOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149209"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="cd894-106">Propiedad GetVolumeOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="cd894-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="cd894-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) .</span><span class="sxs-lookup"><span data-stu-id="cd894-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="cd894-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cd894-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd894-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd894-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="cd894-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cd894-110">Property value</span></span>

<span data-ttu-id="cd894-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="cd894-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd894-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd894-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd894-113">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="cd894-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 