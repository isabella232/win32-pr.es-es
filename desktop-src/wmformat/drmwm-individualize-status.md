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
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS estructura (wmdrmsdk. h)

La estructura de estado de la **\_ \_ individualización de WM** contiene información sobre un proceso de individualización pendiente.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**h**
</dt> <dd>

Código de retorno **HRESULT** .

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valor del tipo de enumeración de [**\_ \_ Estado de individualización de DRM**](drmdrm-individualization-status.md) que indica el estado actual del proceso de individualización.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntero a una cadena terminada en null que contiene la dirección URL de respuesta de la individualización.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Número de recorridos de ida y vuelta HTTP al servicio de individualización que se han completado.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor del tipo de enumeración de [**\_ \_ Estado http de DRM**](drmdrm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Número de bytes descargados.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Número total de bytes que se van a descargar. Puede usar este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique qué parte de la descarga se ha completado y cuánto queda por hacer.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se recibe cuando se llama al método [**IWMDRMIndividualizationStatus:: getStatus**](iwmdrmindividualizationstatus-getstatus.md) . Contiene el estado del proceso de individualización pendiente en el momento de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





