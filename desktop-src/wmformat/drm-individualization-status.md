---
title: Enumeración DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: El \_ \_ tipo de enumeración estado de individualización de DRM define los Estados válidos para la individualización DRM. | Enumeración DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424292"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="bc948-106">Enumeración DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="bc948-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="bc948-107">El tipo de enumeración **\_ \_ Estado de individualización de DRM** define los Estados válidos para la [*individualización*](wmformat-glossary.md)DRM.</span><span class="sxs-lookup"><span data-stu-id="bc948-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="bc948-108">Cuando una aplicación inicia la individualización con una llamada a [**IWMDRMReader:: individualizate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), el progreso de la solicitud de individualización se transmite a la aplicación a través de las llamadas al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="bc948-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="bc948-109">Todos los mensajes de estado de la individualización usarán el \_ miembro de usuario de WMT del tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) como parámetro *status* .</span><span class="sxs-lookup"><span data-stu-id="bc948-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="bc948-110">El estado de la individualización se pasa a **Alstatus** en el parámetro *pValue* .</span><span class="sxs-lookup"><span data-stu-id="bc948-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc948-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc948-111">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="bc948-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc948-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc948-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDIr \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="bc948-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-114">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bc948-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="bc948-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Inicio de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-116">Indica el inicio del proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="bc948-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="bc948-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ correctamente**</span><span class="sxs-lookup"><span data-stu-id="bc948-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-118">Indica que se ha completado el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="bc948-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="bc948-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**error de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-120">Indica que se ha producido un error en el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="bc948-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="bc948-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**cancelación de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-122">Indica que el proceso de individualización se canceló como resultado de una llamada a [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span><span class="sxs-lookup"><span data-stu-id="bc948-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="bc948-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**descarga de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-124">Indica que se está descargando la actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bc948-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="bc948-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**instalación de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="bc948-126">Indica que se está instalando la actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bc948-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc948-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc948-127">Remarks</span></span>

<span data-ttu-id="bc948-128">Esta enumeración se usa en la estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de WM.</span><span class="sxs-lookup"><span data-stu-id="bc948-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc948-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc948-129">Requirements</span></span>



| <span data-ttu-id="bc948-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc948-130">Requirement</span></span> | <span data-ttu-id="bc948-131">Value</span><span class="sxs-lookup"><span data-stu-id="bc948-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc948-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc948-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc948-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc948-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc948-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc948-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc948-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc948-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bc948-136">Versión</span><span class="sxs-lookup"><span data-stu-id="bc948-136">Version</span></span><br/>                  | <span data-ttu-id="bc948-137">SDK de Windows Media Format 7 o versiones posteriores del SDK</span><span class="sxs-lookup"><span data-stu-id="bc948-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="bc948-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc948-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc948-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc948-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc948-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc948-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc948-141">**\_Estado http de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="bc948-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="bc948-142">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="bc948-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





