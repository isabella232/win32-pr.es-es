---
description: El \_ mensaje AGENTSTATUS de línea de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar lineGetAgentStatus para determinar el estado actual del agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Mensaje de LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690739"
---
# <a name="line_agentstatus-message"></a>Mensaje de línea \_ AGENTSTATUS

El mensaje **\_ AGENTSTATUS de línea** de TAPI se envía cuando cambia el estado de un agente ACD en una línea que la aplicación tiene abierta actualmente. La aplicación puede invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar el estado actual del agente.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de la aplicación para el dispositivo de línea en el que ha cambiado el estado del agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador de la dirección en la línea en la que cambió el estado del agente. Un identificador de dirección está asociado de forma permanente a una dirección; el identificador permanece constante en las actualizaciones del sistema operativo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica el estado del agente que ha cambiado; puede ser una combinación de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Si *dwParam2* incluye el \_ bit de estado LINEAGENTSTATUS, *dwParam3* indica el nuevo valor del miembro **dwState** en [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus). De lo contrario, este parámetro se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El mensaje **line \_ AGENTSTATUS** no se envía a las aplicaciones que admiten versiones anteriores de TAPI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




