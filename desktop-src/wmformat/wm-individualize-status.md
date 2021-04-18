---
title: WM_INDIVIDUALIZE_STATUS estructura (Drmexternals. h)
description: La \_ \_ estructura de estado de la individualización de WM registra el estado del proceso de individualización.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS estructura de Windows Media Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705159"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="6df86-104">WM_INDIVIDUALIZE_STATUS estructura (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="6df86-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="6df86-105">La estructura de estado de la **\_ individualización \_ de WM** registra el estado del proceso de [*individualización*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="6df86-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df86-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6df86-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="6df86-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6df86-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6df86-108">**h**</span><span class="sxs-lookup"><span data-stu-id="6df86-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-109">Código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6df86-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="6df86-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="6df86-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-111">Valor del tipo de enumeración [**\_ \_ Estado de individualización de DRM**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="6df86-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="6df86-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="6df86-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-113">Puntero a una cadena terminada en null que contiene la dirección URL de respuesta de la individualización.</span><span class="sxs-lookup"><span data-stu-id="6df86-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="6df86-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="6df86-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-115">**DWORD** que indica el número de recorridos de ida y vuelta http para el servicio de individualización que se han completado.</span><span class="sxs-lookup"><span data-stu-id="6df86-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="6df86-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="6df86-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-117">Valor del tipo de enumeración de [**\_ \_ Estado http de DRM**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="6df86-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="6df86-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="6df86-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-119">**DWORD** que contiene el número de bytes descargados hasta ahora.</span><span class="sxs-lookup"><span data-stu-id="6df86-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="6df86-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="6df86-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="6df86-121">**DWORD** que contiene el número total de bytes que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="6df86-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="6df86-122">Use este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique qué parte de la descarga se ha completado y cuánto queda por hacer.</span><span class="sxs-lookup"><span data-stu-id="6df86-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6df86-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6df86-123">Remarks</span></span>

<span data-ttu-id="6df86-124">Los componentes de tiempo de ejecución de DRM rellenan esta estructura y se envían a las aplicaciones en el parámetro *pValue* del método Applications [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) cuando el evento es igual a la función WMT \_ .</span><span class="sxs-lookup"><span data-stu-id="6df86-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="6df86-125">La aplicación recibe este evento varias veces durante el proceso de descarga.</span><span class="sxs-lookup"><span data-stu-id="6df86-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df86-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df86-126">Requirements</span></span>



| <span data-ttu-id="6df86-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df86-127">Requirement</span></span> | <span data-ttu-id="6df86-128">Value</span><span class="sxs-lookup"><span data-stu-id="6df86-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df86-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6df86-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6df86-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6df86-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6df86-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6df86-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6df86-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6df86-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6df86-133">Versión</span><span class="sxs-lookup"><span data-stu-id="6df86-133">Version</span></span><br/>                  | <span data-ttu-id="6df86-134">SDK de Windows Media Format 7 o versiones posteriores del SDK</span><span class="sxs-lookup"><span data-stu-id="6df86-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="6df86-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6df86-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df86-136"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df86-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df86-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6df86-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df86-138">**\_Estado http de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6df86-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="6df86-139">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="6df86-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





