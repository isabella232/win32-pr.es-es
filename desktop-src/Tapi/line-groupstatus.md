---
description: El mensaje LINE GROUPSTATUS se envía cuando cambia el estado de un grupo de ACD en un controlador de agente para el que la aplicación tiene actualmente \_ una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c70ba4badd27b4d42774549b4778bd77dda13f0ae7245ee6852c2b3afab164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761948"
---
# <a name="line_groupstatus-message"></a>Mensaje \_ DE LINE GROUPSTATUS

El **mensaje \_ LINE GROUPSTATUS se** envía cuando cambia el estado de un grupo de ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la [**función lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación al dispositivo de línea. Esto está relacionado con el controlador del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado del grupo que ha cambiado. La aplicación puede invocar [**lineGetGroupList para**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) determinar los cambios en los grupos disponibles. El *parámetro dwParam2* es una o varias de las [**constantes LINEGROUPSTATUS \_**](linegroupstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




