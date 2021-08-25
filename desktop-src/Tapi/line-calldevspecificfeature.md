---
description: El mensaje TSPI LINE CALLDEVSPECIFICFEATURE se envía a la función de devolución de llamada LINEEVENT para notificar a TAPI sobre los eventos específicos del dispositivo que se producen en una línea \_ o dirección.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: LINE_CALLDEVSPECIFICFEATURE mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8dde8377f952f02f021209b01f846ba323cc7dbf8795743422e2c83e457b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873635"
---
# <a name="line_calldevspecificfeature-message"></a>MENSAJE \_ LINE CALLDEVSPECIFICFEATURE

El mensaje TSPI **LINE \_ CALLDEVSPECIFICFEATURE** se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre los eventos específicos del dispositivo que se producen en una línea o dirección. El significado del mensaje y la interpretación de los *parámetros dwParam1* a *dwParam3* son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

El identificador de objeto opaco TAPI al dispositivo de línea.

</dd> <dt>

*htCall* 
</dt> <dd>

El identificador de objeto opaco TAPI al dispositivo de llamada.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valor LINE \_ CALLDEVSPECIFICFEATURE.

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

Un proveedor de servicios usa el mensaje **LINE \_ CALLDEVSPECIFICFEATURE** junto con la función [**\_ lineDevSpecificFeature de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) Su significado es específico del dispositivo.

TAPI envía el [**mensaje \_ LINE DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) a las aplicaciones en respuesta a la recepción de este mensaje de un proveedor de servicios. Los *parámetros htLine* y *htCall* se traducen al *hCall adecuado* como el parámetro *hDevice* en el nivel TAPI. Los *parámetros dwParam1,* *dwParam2* y *dwParam3* se pasan a través de sin modificar.

No hay ningún mensaje directamente correspondiente en el nivel TAPI, aunque este mensaje es muy similar a LINE \_ DEVSPECIFICFEATURE. En el nivel de TSPI, los mensajes de características específicos del dispositivo se dividen entre los eventos de informes en líneas y direcciones, y los eventos de informes en las llamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**Línea \_ TSPIDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

