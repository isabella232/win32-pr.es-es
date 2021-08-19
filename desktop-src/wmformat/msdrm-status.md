---
title: MSDRM_STATUS enumeración (Wmdrmsdk.h)
description: El tipo de enumeración MSDRM \_ STATUS define las condiciones de estado para el subsistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS enumeración windows Media Format
- enumeración windows Media Format
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4c1f9b37f237b1ae2399849ef3100e3d6fdbc12c7ee3bc1d169420e38bb85a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654579"
---
# <a name="msdrm_status-enumeration"></a>Enumeración MSDRM \_ STATUS

El **tipo de enumeración MSDRM \_ STATUS** define las condiciones de estado para el subsistema DRM.

## <a name="syntax"></a>Syntax


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**\_ERROR DE DRM**
</dt> <dd>

Especifica que se ha producido un error.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**INFORMACIÓN DE \_ DRM**
</dt> <dd>

Especifica que hay información de estado adicional.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM \_ BACKUPRESTORE \_ BEGIN**
</dt> <dd>

Especifica que se ha iniciado una operación de copia de seguridad o restauración de licencias.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM \_ BACKUPRESTORE \_ END**
</dt> <dd>

Especifica que ha finalizado una operación de copia de seguridad o restauración de licencias.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM \_ BACKUPRESTORE \_ CONNECTING**
</dt> <dd>

Especifica que hay una operación de copia de seguridad o restauración de licencias en curso y que el equipo cliente se conecta con el servidor de copia de seguridad.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM \_ BACKUPRESTORE \_ DISCONNECTING**
</dt> <dd>

Especifica que hay una operación de copia de seguridad o restauración de licencias en curso y que el equipo cliente se desconecta del servidor de copia de seguridad.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**ERROR DE DRM \_ \_ WITHURL**
</dt> <dd>

Especifica que la operación DRM ha encontrado una dirección URL no válida.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**LICENCIA \_ RESTRINGIDA DE DRM \_**
</dt> <dd>

Especifica que la operación drm no puede continuar porque no existe ninguna licencia que conceda el derecho necesario en el equipo cliente.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ NECESITA \_ INDIVIDUALIZACIÓN**
</dt> <dd>

Especifica que la operación drm no puede continuar porque el subsistema DRM debe individualizarse.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**NOTIFICACIÓN \_ DE \_ OPL DE REPRODUCCIÓN DE DRM \_**
</dt> <dd>

Especifica que no se puede completar una operación de reproducción porque no se ha cumplido un requisito de nivel de protección de salida.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**NOTIFICACIÓN DE \_ \_ OPL DE COPIA DE DRM \_**
</dt> <dd>

Especifica que no se puede completar una operación de copia porque no se ha cumplido un requisito de nivel de protección de salida.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM \_ REFRESHCRL \_ COMPLETE**
</dt> <dd>

Especifica que una llamada a [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) ha completado la actualización de una lista de revocación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





