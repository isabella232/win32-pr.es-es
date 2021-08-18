---
title: WM_INDIVIDUALIZE_STATUS estructura (Drternals.h)
description: La estructura WM \_ INDIVIDUALIZE \_ STATUS registra el estado del proceso de individualización.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS windows Media Format de estructura
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
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699025"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS estructura (Drternals.h)

La **estructura WM \_ INDIVIDUALIZE \_ STATUS** registra el estado del [*proceso de individualización.*](wmformat-glossary.md)

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

**Código de retorno HRESULT.**

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valor del tipo [**de enumeración DRM \_ INDIVIDUALIZATION \_ STATUS.**](drm-individualization-status.md)

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene la dirección URL de respuesta de individualización.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** que indica el número de recorridos de ida y vuelta HTTP al servicio de individualización que se han completado.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor del tipo [**de \_ enumeración DRM HTTP \_ STATUS.**](drm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** que contiene el número de bytes descargados hasta ahora.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** que contiene el número total de bytes que se descargarán. Use este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique cuánto de la descarga se ha completado y cuánto queda por hacer.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura la rellenan los componentes en tiempo de ejecución de DRM y se envía a las aplicaciones en el *parámetro pValue* de la aplicación [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) cuando el evento es igual a WMT \_ INDIVIDUALIZE. La aplicación recibe este evento varias veces durante el proceso de descarga.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                      |
| Versión<br/>                  | Windows SDK de formato multimedia 7 o versiones posteriores del SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Drternals.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ESTADO HTTP DE DRM \_ \_**](drm-http-status.md)
</dt> <dt>

[**Estructuras**](structures.md)
</dt> </dl>

 

 





