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
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>Enumeración DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)

El tipo de enumeración **\_ \_ Estado de individualización de DRM** define los Estados válidos para la [*individualización*](wmformat-glossary.md)DRM. Cuando una aplicación inicia la individualización con una llamada a [**IWMDRMReader:: individualizate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), el progreso de la solicitud de individualización se transmite a la aplicación a través de las llamadas al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Todos los mensajes de estado de la individualización usarán el \_ miembro de usuario de WMT del tipo de enumeración [**\_ Estado de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) como parámetro *status* . El estado de la individualización se pasa a **Alstatus** en el parámetro *pValue* .

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

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDIr \_ sin definir**
</dt> <dd>

Este valor está reservado para uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Inicio de INDI \_**
</dt> <dd>

Indica el inicio del proceso de individualización.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ correctamente**
</dt> <dd>

Indica que se ha completado el proceso de individualización.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**error de INDI \_**
</dt> <dd>

Indica que se ha producido un error en el proceso de individualización.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**cancelación de INDI \_**
</dt> <dd>

Indica que el proceso de individualización se canceló como resultado de una llamada a [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**descarga de INDI \_**
</dt> <dd>

Indica que se está descargando la actualización de seguridad.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**instalación de INDI \_**
</dt> <dd>

Indica que se está instalando la actualización de seguridad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | SDK de Windows Media Format 7 o versiones posteriores del SDK<br/>                       |
| Encabezado<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Estado http de DRM \_**](drm-http-status.md)
</dt> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





