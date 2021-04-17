---
title: Código de notificación de TCN_GETOBJECT (commctrl. h)
description: Se envía por un control de pestaña cuando tiene el \_ \_ estilo extendido TCS ex REGISTERDROP y se arrastra un objeto sobre un elemento de ficha del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656454"
---
# <a name="tcn_getobject-notification-code"></a><span data-ttu-id="4c7c1-105">TCN \_ código de notificación GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="4c7c1-105">TCN\_GETOBJECT notification code</span></span>

<span data-ttu-id="4c7c1-106">Se envía por un control de pestaña cuando tiene el estilo extendido [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) y se arrastra un objeto sobre un elemento de ficha del control.</span><span class="sxs-lookup"><span data-stu-id="4c7c1-106">Sent by a tab control when it has the [**TCS\_EX\_REGISTERDROP**](tab-control-extended-styles.md) extended style and an object is dragged over a tab item in the control.</span></span> <span data-ttu-id="4c7c1-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7c1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4c7c1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c7c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c7c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7c1-110">Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el elemento de ficha al que se arrastra el objeto y recibe los datos que devuelve la aplicación en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c7c1-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the tab item the object is dragged over and receives data the application returns in response to this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7c1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c7c1-111">Return value</span></span>

<span data-ttu-id="4c7c1-112">El procesamiento de la aplicación en este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="4c7c1-112">The application processing this notification code must return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7c1-113">Requirements</span></span>



| <span data-ttu-id="4c7c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7c1-114">Requirement</span></span> | <span data-ttu-id="4c7c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="4c7c1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7c1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c7c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7c1-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4c7c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c7c1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c7c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7c1-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c7c1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c7c1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c7c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c7c1-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7c1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





