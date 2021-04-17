---
description: El \_ mensaje line QUEUESTATUS se envía cuando el estado de una cola de ACD cambia en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Mensaje de LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690503"
---
# <a name="line_queuestatus-message"></a>Mensaje de línea \_ QUEUESTATUS

El mensaje **line \_ QUEUESTATUS** se envía cuando el estado de una cola de ACD cambia en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


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

El identificador de la cola cuyo estado ha cambiado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado de la cola que ha cambiado. Puede ser una o varias de las [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

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

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




