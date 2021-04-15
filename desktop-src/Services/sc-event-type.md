---
description: Indica un tipo de cambio de estado de servicio para la supervisión y la generación de informes.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Enumeración SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669723"
---
# <a name="sc_event_type-enumeration"></a>\_Enumeración de tipo de evento SC \_

Indica un tipo de cambio de estado de servicio para la supervisión y la generación de informes.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**cambio en la \_ base de datos de eventos SC \_ \_**
</dt> <dd>

Se ha agregado o eliminado un servicio. El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del SCM.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_cambio de \_ propiedad de evento de SC \_**
</dt> <dd>

Se han actualizado una o varias propiedades de servicio. El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del servicio.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_cambio de \_ Estado de evento de SC \_**
</dt> <dd>

El estado de un servicio ha cambiado. El parámetro *hService* de la función [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) debe ser un identificador del servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl> |



 

 




