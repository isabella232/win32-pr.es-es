---
title: WINBIO_INDICATOR_STATUS constantes (Winbio \_ types.h)
description: Establecer una luz indicadora.
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
ms.openlocfilehash: 9fd05d279bd11eafda89eed436c94d6141e97ad0eb9d2fc426d5c89000f36414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910018"
---
# <a name="winbio_indicator_status-constants"></a>Constantes DE \_ ESTADO DE INDICADOR DE WINBIO \_

Los valores siguientes se pueden usar para establecer una luz indicadora. De forma predeterminada, los sensores no tendrán una luz encendido, pero las aplicaciones pueden usar estos valores para habilitar o deshabilitar las luces indicadoras. El **valor DE ESTADO DEL SENSOR \_ \_ WINBIO** proporciona más detalles sobre el estado de una luz indicadora que está encendido. Para obtener más información, vea las siguientes funciones:

-   [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)
-   [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)
-   [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)



| Constante                                                                                                                                                                            | Descripción                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------|
| <span id="WINBIO_INDICATOR_ON"></span><span id="winbio_indicator_on"></span><dl> <dt>**INDICADOR WINBIO \_ \_ ON**</dt> </dl>    | La luz indicadora del sensor está encendido.<br/>  |
| <span id="WINBIO_INDICATOR_OFF"></span><span id="winbio_indicator_off"></span><dl> <dt>**INDICADOR WINBIO \_ \_ DESACTIVADO**</dt> </dl> | La luz indicadora del sensor está apagada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





