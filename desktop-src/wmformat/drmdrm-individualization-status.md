---
title: DRM_INDIVIDUALIZATION_STATUS enumeración (Wmdrmsdk.h)
description: El tipo de enumeración DRM \_ INDIVIDUALIZATION \_ STATUS define los estados válidos para la individualización de DRM. | DRM_INDIVIDUALIZATION_STATUS enumeración (Wmdrmsdk.h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS de enumeración windows Media Format
- enumeración windows Media Format
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
ms.openlocfilehash: 47e339fda95ccf7408ad2f218179cfb591da217b16fbbce9c9870eabd7437eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848231"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>DRM_INDIVIDUALIZATION_STATUS enumeración (Wmdrmsdk.h)

El **tipo de enumeración DRM \_ INDIVIDUALIZATION \_ STATUS** define los estados válidos para la individualización de DRM.

## <a name="syntax"></a>Syntax


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

Indica que se ha fallado el proceso de individualización.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ CANCEL**
</dt> <dd>

Indica que la aplicación canceló el proceso de individualización.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**DESCARGA \_ DE INDI**
</dt> <dd>

Indica que se está descargando la actualización de seguridad.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**INSTALACIÓN \_ DE INDI**
</dt> <dd>

Indica que se está instalando la actualización de seguridad.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La estructura WM [**\_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) utiliza esta enumeración.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





