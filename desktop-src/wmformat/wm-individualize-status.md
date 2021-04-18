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
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS estructura (Drmexternals. h)

La estructura de estado de la **\_ individualización \_ de WM** registra el estado del proceso de [*individualización*](wmformat-glossary.md) .

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

Valor del tipo de enumeración [**\_ \_ Estado de individualización de DRM**](drm-individualization-status.md) .

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntero a una cadena terminada en null que contiene la dirección URL de respuesta de la individualización.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** que indica el número de recorridos de ida y vuelta http para el servicio de individualización que se han completado.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor del tipo de enumeración de [**\_ \_ Estado http de DRM**](drm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** que contiene el número de bytes descargados hasta ahora.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** que contiene el número total de bytes que se van a descargar. Use este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique qué parte de la descarga se ha completado y cuánto queda por hacer.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los componentes de tiempo de ejecución de DRM rellenan esta estructura y se envían a las aplicaciones en el parámetro *pValue* del método Applications [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) cuando el evento es igual a la función WMT \_ . La aplicación recibe este evento varias veces durante el proceso de descarga.

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

[**Estructuras**](structures.md)
</dt> </dl>

 

 





