---
description: El mensaje CALLDEVSPECIFIC de la línea de TSPI \_ se envía a la función de devolución de llamada LINEEVENT para notificar a TAPI los eventos específicos del dispositivo que se producen en una llamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Mensaje de LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680182"
---
# <a name="line_calldevspecific-message"></a>Mensaje de línea \_ CALLDEVSPECIFIC

El mensaje **\_ CALLDEVSPECIFIC** de la línea de TSPI se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI los eventos específicos del dispositivo que se producen en una llamada. El significado del mensaje y la interpretación de los parámetros de *dwParam1* a través de *dwParam3* son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

El identificador de objeto opaco TAPI para el dispositivo de línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador de objeto opaco TAPI para el dispositivo de llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La línea de valor \_ CALLDEVSPECIFIC.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico del dispositivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un proveedor de servicios usa el mensaje **line \_ CALLDEVSPECIFIC** junto con la función [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) . Su significado es específico del dispositivo.

TAPI envía el mensaje [**line \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) a las aplicaciones en respuesta a la recepción de este mensaje de un proveedor de servicios. Los parámetros *htLine* y *htCall* se traducen a la *HCall* adecuada como el parámetro *hDevice* en el nivel de TAPI. Los parámetros *dwParam1*, *dwParam2* y *dwParam3* se pasan sin modificar.

No hay ningún mensaje directamente correspondiente en el nivel de TAPI, aunque este mensaje es muy similar a la [**línea \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)). En el nivel de TSPI, los mensajes específicos del dispositivo se dividen entre los eventos de informes en líneas y direcciones, y los eventos de informes en llamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

