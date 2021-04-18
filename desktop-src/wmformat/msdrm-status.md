---
title: Enumeración MSDRM_STATUS (wmdrmsdk. h)
description: El \_ tipo de enumeración de estado MSDRM define las condiciones de estado para el subsistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
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
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721589"
---
# <a name="msdrm_status-enumeration"></a>\_Enumeración de estado de MSDRM

El tipo de enumeración de **\_ Estado MSDRM** define las condiciones de estado para el subsistema DRM.

## <a name="syntax"></a>Sintaxis


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

<span id="DRM_ERROR"></span><span id="drm_error"></span>**ERROR de DRM \_**
</dt> <dd>

Especifica que se ha producido un error.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**información de DRM \_**
</dt> <dd>

Especifica que hay información de estado adicional.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_Inicio de BACKUPRESTORE de DRM \_**
</dt> <dd>

Especifica que se ha iniciado una operación de restauración o copia de seguridad de licencias.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_final de BACKUPRESTORE DRM \_**
</dt> <dd>

Especifica que ha finalizado una operación de copia de seguridad o restauración de una licencia.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_conexión de BACKUPRESTORE DRM \_**
</dt> <dd>

Especifica que una operación de copia de seguridad o restauración de licencias está en curso y que el equipo cliente se está conectando con el servidor de copia de seguridad.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**desconexión de BACKUPRESTORE de DRM \_ \_**
</dt> <dd>

Especifica que una operación de copia de seguridad o restauración de licencias está en curso y que el equipo cliente se está desconectando del servidor de copia de seguridad.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_error \_ WITHURL de DRM**
</dt> <dd>

Especifica que la operación DRM ha encontrado una dirección URL incorrecta.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**licencia de DRM \_ restringida \_**
</dt> <dd>

Especifica que la operación DRM no puede continuar porque no existe ninguna licencia que conceda el derecho necesario en el equipo cliente.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ necesita la \_ individualización**
</dt> <dd>

Especifica que la operación DRM no puede continuar porque el subsistema DRM debe ser individualizado.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_notificación del \_ OPL de reproducción de DRM \_**
</dt> <dd>

Especifica que no se puede completar una operación de reproducción porque no se ha cumplido un requisito de nivel de protección de salida.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_notificación del \_ OPL de copia de DRM \_**
</dt> <dd>

Especifica que no se puede completar una operación de copia porque no se ha cumplido un requisito de nivel de protección de salida.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**REFRESHCRL de DRM \_ \_ completado**
</dt> <dd>

Especifica que una llamada a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) ha completado la actualización de una lista de revocación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](drm-enumeration-types.md)
</dt> </dl>

 

 





