---
description: El mensaje TSPI LINE CALLDEVSPECIFIC se envía a la función de devolución de llamada LINEEVENT para notificar a TAPI sobre los eventos específicos del dispositivo que se producen \_ en una llamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9930da3c30d51781b10b28ed7a712cb681950eaea1a387212a5e0894658a9125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012605"
---
# <a name="line_calldevspecific-message"></a>MENSAJE \_ LINE CALLDEVSPECIFIC

El mensaje TSPI **LINE \_ CALLDEVSPECIFIC** se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre los eventos específicos del dispositivo que se producen en una llamada. El significado del mensaje y la interpretación de los *parámetros dwParam1* a *dwParam3* son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador de objeto opaco TAPI para el dispositivo de línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Identificador de objeto opaco TAPI para el dispositivo de llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valor LINE \_ CALLDEVSPECIFIC.

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

## <a name="remarks"></a>Comentarios

Un proveedor de servicios usa el mensaje **LINE \_ CALLDEVSPECIFIC** junto con la función [**\_ lineDevSpecific de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) Su significado es específico del dispositivo.

TAPI envía el [**mensaje \_ LINE DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) a las aplicaciones en respuesta a recibir este mensaje de un proveedor de servicios. Los *parámetros htLine* *y htCall* se traducen al *hCall adecuado* como el parámetro *hDevice* en el nivel TAPI. Los *parámetros dwParam1,* *dwParam2* y *dwParam3* se pasan a través de sin modificar.

No hay ningún mensaje directamente correspondiente en el nivel TAPI, aunque este mensaje es muy similar a [**LINE \_ DEVSPECIFIC.**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) En el nivel de TSPI, los mensajes específicos del dispositivo se dividen entre los eventos de informes en líneas y direcciones, y los eventos de informes en las llamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**Línea \_ TSPIDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

