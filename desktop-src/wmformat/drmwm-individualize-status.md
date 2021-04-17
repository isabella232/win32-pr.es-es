---
title: WM_INDIVIDUALIZE_STATUS estructura (wmdrmsdk. h)
description: La estructura de estado de la \_ individualización de WM \_ contiene información sobre un proceso de individualización pendiente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS estructura de Windows Media Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708868"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="5cb58-104">WM_INDIVIDUALIZE_STATUS estructura (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="5cb58-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="5cb58-105">La estructura de estado de la **\_ \_ individualización de WM** contiene información sobre un proceso de individualización pendiente.</span><span class="sxs-lookup"><span data-stu-id="5cb58-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cb58-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cb58-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="5cb58-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5cb58-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5cb58-108">**h**</span><span class="sxs-lookup"><span data-stu-id="5cb58-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-109">Código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5cb58-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="5cb58-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-111">Valor del tipo de enumeración de [**\_ \_ Estado de individualización de DRM**](drmdrm-individualization-status.md) que indica el estado actual del proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="5cb58-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="5cb58-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-113">Puntero a una cadena terminada en null que contiene la dirección URL de respuesta de la individualización.</span><span class="sxs-lookup"><span data-stu-id="5cb58-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="5cb58-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-115">Número de recorridos de ida y vuelta HTTP al servicio de individualización que se han completado.</span><span class="sxs-lookup"><span data-stu-id="5cb58-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="5cb58-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-117">Valor del tipo de enumeración de [**\_ \_ Estado http de DRM**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb58-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="5cb58-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-119">Número de bytes descargados.</span><span class="sxs-lookup"><span data-stu-id="5cb58-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="5cb58-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="5cb58-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="5cb58-121">Número total de bytes que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="5cb58-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="5cb58-122">Puede usar este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique qué parte de la descarga se ha completado y cuánto queda por hacer.</span><span class="sxs-lookup"><span data-stu-id="5cb58-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cb58-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cb58-123">Remarks</span></span>

<span data-ttu-id="5cb58-124">Esta estructura se recibe cuando se llama al método [**IWMDRMIndividualizationStatus:: getStatus**](iwmdrmindividualizationstatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5cb58-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="5cb58-125">Contiene el estado del proceso de individualización pendiente en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5cb58-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb58-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cb58-126">Requirements</span></span>



| <span data-ttu-id="5cb58-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb58-127">Requirement</span></span> | <span data-ttu-id="5cb58-128">Value</span><span class="sxs-lookup"><span data-stu-id="5cb58-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb58-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cb58-129">Header</span></span><br/> | <dl> <span data-ttu-id="5cb58-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb58-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb58-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cb58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb58-132">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="5cb58-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





