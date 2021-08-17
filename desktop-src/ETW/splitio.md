---
description: Esta clase es la clase primaria para los eventos de E/S divididos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069725"
---
# <a name="splitio-class"></a>SplitIo (clase)

Esta clase es la clase primaria para los eventos de E/S divididos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La **clase SplitIo** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para habilitar los eventos de E/S divididos en una sesión de registro del kernel de NT, especifique la marca **EVENT TRACE FLAG SPLIT \_ \_ \_ \_ IO** en el miembro **EnableFlags** de una estructura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la [**función StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para eventos de E/S divididos llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**SplitIoGuid**](nt-kernel-logger-constants.md) como *parámetro pGuid.* Use el siguiente tipo de evento para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valor de tipo de evento, 32 | Evento de E/S dividida. La [**clase MOF SplitIo \_ Info**](splitio-info.md) define los datos de evento para este evento. |



 

Los eventos de E/S de división indican que las solicitudes de E/S se han dividido en varias solicitudes de E/S de disco debido al hardware de disco de creación de reflejo subyacente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 
