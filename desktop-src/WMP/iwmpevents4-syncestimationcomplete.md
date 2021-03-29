---
title: IWMPEvents4 SyncEstimationComplete, método
description: El evento SyncEstimationComplete se produce cuando se completa una estimación de tamaño, iniciada anteriormente por IWMPSyncDevice3 estimateSyncSize.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Método SyncEstimationComplete de Windows Media Player
- Método SyncEstimationComplete Windows Media Player, interfaz IWMPEvents4
- Interfaz IWMPEvents4 Windows Media Player, método SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788679"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4:: SyncEstimationComplete (método)

El evento **SyncEstimationComplete** se produce cuando se completa una estimación de tamaño, iniciada anteriormente por [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).

## <a name="syntax"></a>Sintaxis


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Puntero a la interfaz [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) que representa el dispositivo para el que se inició la estimación del tamaño.

</dd> <dt>

*hrResult* \[ de\]
</dt> <dd>

Valor que indica si la estimación se ha realizado correctamente o no.



| Value                                                                                                                                       | Significado                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ correcto**</dt> </dl>          | La estimación se ha realizado correctamente.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ anular**</dt> </dl> | Se anuló la estimación.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ de\]
</dt> <dd>

Espacio Estimado (en bytes) que se utilizaría en el dispositivo.

</dd> <dt>

*lEstimatedSize* \[ de\]
</dt> <dd>

Tamaño estimado (en bytes) de los datos que se van a sincronizar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





