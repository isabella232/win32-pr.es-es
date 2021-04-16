---
title: Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración estado de individualización de DRM define los Estados válidos para la individualización DRM. | Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671493"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)

El tipo de enumeración **\_ \_ Estado de individualización de DRM** define los Estados válidos para la individualización DRM.

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

Indica que la aplicación canceló el proceso de individualización.

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

Esta enumeración se usa en la estructura de [**\_ \_ Estado**](drmwm-individualize-status.md) de la función de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





