---
title: DRM_INDIVIDUALIZATION_STATUS enumeración (Drternals.h)
description: El tipo de enumeración ESTADO DE INDIVIDUALIZACIÓN DE DRM \_ define los estados \_ válidos para la individualización de DRM. | DRM_INDIVIDUALIZATION_STATUS enumeración (Drternals.h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeración windows Media Format
- enumeración windows Media Format
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247383"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>DRM_INDIVIDUALIZATION_STATUS enumeración (Drternals.h)

El **tipo de enumeración DRM \_ INDIVIDUALIZATION \_ STATUS** define los estados válidos para [*la individualización de*](wmformat-glossary.md)DRM. Cuando una aplicación inicia la individualización con una llamada a [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), el progreso de la solicitud de individualización se transmite a la aplicación a través de llamadas al método [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Todos los mensajes de estado de individualización usarán el miembro WMT INDIVIDUALIZE del tipo de enumeración STATUS de \_ [**WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) como *parámetro Status.* El estado de la individualización se pasa a **OnStatus** en el *parámetro pValue.*

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ UNDEFINED**
</dt> <dd>

Este valor está reservado para uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ BEGIN**
</dt> <dd>

Indica el inicio del proceso de individualización.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ SUCCEED**
</dt> <dd>

Indica que se ha completado el proceso de individualización.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**ERROR \_ DE INDI**
</dt> <dd>

Indica que error en el proceso de individualización.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ CANCEL**
</dt> <dd>

Indica que el proceso de individualización se canceló como resultado de una llamada a [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**DESCARGA \_ DE INDI**
</dt> <dd>

Indica que se está descargando la actualización de seguridad.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**INSTALACIÓN \_ DE INDI**
</dt> <dd>

Indica que se está instalando la actualización de seguridad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la utiliza la [**estructura WM \_ INDIVIDUALIZE \_ STATUS.**](wm-individualize-status.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drternals.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADO HTTP DE DRM \_ \_**](drm-http-status.md)
</dt> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





