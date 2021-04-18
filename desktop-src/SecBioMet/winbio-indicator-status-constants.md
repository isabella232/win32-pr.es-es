---
title: Constantes de WINBIO_INDICATOR_STATUS (Winbio \_ Types. h)
description: Establecer una luz del indicador.
ms.assetid: 1e00ff9d-6693-4763-8ac3-b42d2a3e987d
topic_type:
- apiref
api_name:
- WINBIO_INDICATOR_ON
- WINBIO_INDICATOR_OFF
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7693fbd2b9b37067738774d172f4bb482edb06e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686246"
---
# <a name="winbio_indicator_status-constants"></a>Constantes de estado de \_ indicador de WINBIO \_

Los valores siguientes se pueden usar para establecer una luz del indicador. De forma predeterminada, los sensores no tendrán una luz encendida, pero las aplicaciones pueden usar estos valores para habilitar o deshabilitar las luces de indicador. El valor de **\_ \_ Estado del sensor de WINBIO** proporciona más detalles sobre el estado de una luz del indicador activada. Para obtener más información, vea las siguientes funciones:

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Constante                                                                                                                                                                            | Descripción                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**\_indicador \_ de WINBIO en**</dt> </dl>    | La luz del indicador del sensor está activada.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**indicador de WINBIO \_ \_ desactivado**</dt> </dl> | La luz del indicador del sensor está desactivada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





