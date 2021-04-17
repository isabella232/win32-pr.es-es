---
description: Obtiene información sobre qué columnas (tipos de datos de eventos) se admiten en la lista de eventos.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsCallback:: GetSupportedEventColumns (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495209"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="f053f-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback:: GetSupportedEventColumns (método)</span><span class="sxs-lookup"><span data-stu-id="f053f-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="f053f-104">Obtiene información sobre qué columnas (tipos de datos de eventos) se admiten en la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f053f-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f053f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f053f-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="f053f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f053f-106">Parameters</span></span>

<span data-ttu-id="f053f-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="f053f-107">*numColumns* </span></span>  
<span data-ttu-id="f053f-108">El número de columnas admitidas por</span><span class="sxs-lookup"><span data-stu-id="f053f-108">The number of columns supported by</span></span>

<span data-ttu-id="f053f-109">*count0 \_ PID* </span><span class="sxs-lookup"><span data-stu-id="f053f-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="f053f-110">Los identificadores de cada columna que admite la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f053f-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="f053f-111">*count0 \_ pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="f053f-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="f053f-112">Los nombres de cada columna, como una cadena COM, que admite la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="f053f-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="f053f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f053f-113">Return value</span></span>

<span data-ttu-id="f053f-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f053f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f053f-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f053f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f053f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f053f-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f053f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f053f-117">Header</span></span></p></td><td><span data-ttu-id="f053f-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f053f-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f053f-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="f053f-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f053f-120">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="f053f-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
