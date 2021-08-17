---
description: El mensaje LINE QUEUESTATUS se envía cuando cambia el estado de una cola de ACD en un controlador de agente para el que la aplicación tiene actualmente \_ una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336a8239e31e5c0bcc70de747cbb48a2028c85e67f44a3e45032f02b37065d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975535"
---
# <a name="line_queuestatus-message"></a>Mensaje \_ LINE QUEUESTATUS

El **mensaje \_ LINE QUEUESTATUS se** envía cuando cambia el estado de una cola de ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la [**función lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


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

Identificador de la cola cuyo estado ha cambiado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado de la cola que ha cambiado. Puede ser una o varias de las [**constantes LINEQUEUESTATUS \_**](linequeuestatus--constants.md).

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




