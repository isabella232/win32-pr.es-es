---
title: WM_INDIVIDUALIZE_STATUS estructura (Wmdrmsdk.h)
description: La estructura WM \_ INDIVIDUALIZE \_ STATUS contiene información sobre un proceso de individualización pendiente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS structure windows Media Format
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
ms.openlocfilehash: c139631fe737e07d011e43920ab63c7394f03c3319abb2f7936153ae06c596ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708305"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS estructura (Wmdrmsdk.h)

La **estructura WM \_ INDIVIDUALIZE \_ STATUS** contiene información sobre un proceso de individualización pendiente.

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

Valor del tipo [**de enumeración DRM \_ INDIVIDUALIZATION \_ STATUS**](drmdrm-individualization-status.md) que indica el estado actual del proceso de individualización.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene la dirección URL de respuesta de individualización.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Número de recorridos de ida y vuelta HTTP al servicio de individualización que se han completado.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor del tipo [**de \_ enumeración DRM HTTP \_ STATUS.**](drmdrm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Número de bytes descargados.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Número total de bytes que se descargarán. Puede usar este valor y **dwHTTPReadProgress** para mostrar una interfaz de usuario que indique cuánto se ha completado la descarga y cuánto queda por hacer.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se recibe cuando se llama al [**método IWMDRMIndividualizationStatus::GetStatus.**](iwmdrmindividualizationstatus-getstatus.md) Contiene el estado del proceso de individualización pendiente en el momento de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras**](drm-structures.md)
</dt> </dl>

 

 





