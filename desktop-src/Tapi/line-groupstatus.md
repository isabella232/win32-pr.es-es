---
description: El \_ mensaje line GROUPSTATUS se envía cuando cambia el estado de un grupo ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Mensaje de LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679467"
---
# <a name="line_groupstatus-message"></a>Mensaje de línea \_ GROUPSTATUS

El mensaje **line \_ GROUPSTATUS** se envía cuando cambia el estado de un grupo ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea. Esto se relaciona con el controlador del agente.

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

Especifica el estado del grupo que ha cambiado. La aplicación puede invocar [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) para determinar los cambios en los grupos disponibles. El parámetro *dwParam2* es una o varias de las [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




