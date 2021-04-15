---
title: Método GetStatus de IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: El método GetStatus recupera información detallada sobre el progreso de la individualización.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Método GetStatus formato de Windows Media
- Método GetStatus formato de Windows Media, interfaz IWMDRMIndividualizationStatus
- Interfaz IWMDRMIndividualizationStatus formato de Windows Media, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708897"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>IWMDRMIndividualizationStatus:: GetStatus (método)

El método **getStatus** recupera información detallada sobre el progreso de la individualización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStatus* \[ enuncia\]
</dt> <dd>

Recibe una estructura de [**\_ \_ Estado de usuario de WM**](drmwm-individualize-status.md) que contiene información detallada sobre el estado del intento de individualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





