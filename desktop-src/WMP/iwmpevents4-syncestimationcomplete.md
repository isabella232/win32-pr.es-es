---
title: Método IWMPEvents4 SyncEstimationComplete
description: El evento SyncEstimationComplete tiene lugar cuando se completa una estimación de tamaño iniciada anteriormente por IWMPSyncDevice3 estimateSyncSize.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Método SyncEstimationComplete Reproductor de Windows Media
- Método SyncEstimationComplete Reproductor de Windows Media , interfaz IWMPEvents4
- Interfaz IWMPEvents4 Reproductor de Windows Media , método SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3f444cdc66874c907bb4c6412fa10384fde67145563d79153c28cb675c6fc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575610"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4::SyncEstimationComplete (método)

El **evento SyncEstimationComplete** tiene lugar cuando se completa una estimación de tamaño, iniciada anteriormente por [**IWMPSyncDevice3::estimateSyncSize.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)

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

*pDevice* \[ En\]
</dt> <dd>

Puntero a la [**interfaz IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) que representa el dispositivo para el que se inició la estimación de tamaño.

</dd> <dt>

*hrResult* \[ En\]
</dt> <dd>

Valor que indica el éxito o el error de la estimación.



| Valor                                                                                                                                       | Significado                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>          | La estimación se ha logrado correctamente.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ ABORT**</dt> </dl> | Se anuló la estimación.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ En\]
</dt> <dd>

Espacio estimado (en bytes) que se usaría en el dispositivo.

</dd> <dt>

*lEstimatedSize* \[ En\]
</dt> <dd>

Tamaño estimado (en bytes) de los datos que se sincronizarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPEvents4 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





