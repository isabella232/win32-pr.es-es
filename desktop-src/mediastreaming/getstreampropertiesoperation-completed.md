---
title: Propiedad GetStreamPropertiesOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetStreamPropertiesAsync.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz GetStreamPropertiesOperation
- Interfaz GetStreamPropertiesOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420613"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="dc02a-106">Propiedad GetStreamPropertiesOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="dc02a-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="dc02a-107">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc02a-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="dc02a-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dc02a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc02a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc02a-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="dc02a-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc02a-110">Property value</span></span>

<span data-ttu-id="dc02a-111">Controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="dc02a-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc02a-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc02a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc02a-113">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="dc02a-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 