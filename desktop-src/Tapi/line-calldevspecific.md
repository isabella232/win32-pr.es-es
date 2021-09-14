---
description: El mensaje TSPI LINE CALLDEVSPECIFIC se envía a la función de devolución de llamada LINEEVENT para notificar a TAPI sobre los eventos específicos del dispositivo que se producen \_ en una llamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250220"
---
# <a name="line_calldevspecific-message"></a>MENSAJE \_ LINE CALLDEVSPECIFIC

El mensaje TSPI **LINE \_ CALLDEVSPECIFIC** se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre los eventos específicos del dispositivo que se producen en una llamada. El significado del mensaje y la interpretación de los *parámetros dwParam1* a *dwParam3* son específicos del dispositivo.


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

## <a name="remarks"></a>Observaciones

Un proveedor de servicios usa el mensaje **LINE \_ CALLDEVSPECIFIC** junto con la función [**\_ lineDevSpecific de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) Su significado es específico del dispositivo.

TAPI envía el mensaje [**\_ LINE DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) a las aplicaciones en respuesta a la recepción de este mensaje de un proveedor de servicios. Los *parámetros htLine* *y htCall* se traducen al *hCall adecuado* como el parámetro *hDevice* en el nivel TAPI. Los *parámetros dwParam1,* *dwParam2* y *dwParam3* se pasan a través de sin modificar.

No hay ningún mensaje directamente correspondiente en el nivel TAPI, aunque este mensaje es muy similar a [**LINE \_ DEVSPECIFIC.**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) En el nivel de TSPI, los mensajes específicos del dispositivo se dividen entre los eventos de informes en líneas y direcciones, y los eventos de informes en las llamadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**Línea \_ TSPIDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

