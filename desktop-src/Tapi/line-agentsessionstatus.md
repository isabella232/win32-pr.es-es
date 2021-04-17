---
description: El \_ mensaje line AGENTSESSIONSTATUS se envía cuando cambia el estado de una sesión del agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Mensaje de LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690741"
---
# <a name="line_agentsessionstatus-message"></a>Mensaje de línea \_ AGENTSESSIONSTATUS

El mensaje **line \_ AGENTSESSIONSTATUS** se envía cuando cambia el estado de una sesión del agente ACD en un controlador de agente para el que la aplicación tiene actualmente una línea abierta. Este mensaje se genera mediante la función [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado de la sesión del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la sesión del agente cuyo estado ha cambiado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado de la sesión del agente que ha cambiado. Puede ser uno o varios de los **\_ AGENTSESSIONSTATUS de línea**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indica el nuevo valor del estado del agente, que es una de [**las \_ constantes de LINEAGENTSTATEEX**](lineagentstateex--constants.md).

De lo contrario, *dwParam3* se establece en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




