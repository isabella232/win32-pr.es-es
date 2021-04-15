---
title: Propiedad StreamSelectOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por SelectBestStreamAsync.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz StreamSelectOperation
- Interfaz StreamSelectOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714364"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="7f5cd-106">Propiedad StreamSelectOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="7f5cd-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="7f5cd-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7f5cd-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="7f5cd-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7f5cd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f5cd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f5cd-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="7f5cd-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7f5cd-110">Property value</span></span>

<span data-ttu-id="7f5cd-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="7f5cd-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f5cd-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f5cd-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5cd-113">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="7f5cd-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 