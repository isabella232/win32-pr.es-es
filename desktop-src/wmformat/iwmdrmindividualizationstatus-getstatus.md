---
title: Método IWMDRMIndividualizationStatus GetStatus (Wmdrmsdk.h)
description: El método GetStatus recupera información detallada sobre el progreso de la individualización.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Formato multimedia de windows del método GetStatus
- Método GetStatus windows Media Format , interfaz IWMDRMIndividualizationStatus
- IWMDRMIndividualizationStatus interface windows Media Format , GetStatus method
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359913"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>IWMDRMIndividualizationStatus::GetStatus (método)

El **método GetStatus** recupera información detallada sobre el progreso de la individualización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStatus* \[ out\]
</dt> <dd>

Recibe una [**estructura WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) que contiene información detallada sobre el estado del intento de individualización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMIndividualizationStatus (Interfaz)**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





