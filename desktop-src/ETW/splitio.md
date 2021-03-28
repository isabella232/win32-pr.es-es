---
description: Esta clase es la clase primaria para los eventos de e/s divididos. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Clase SplitIo
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
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985082"
---
# <a name="splitio-class"></a>Clase SplitIo

Esta clase es la clase primaria para los eventos de e/s divididos.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Miembros

La clase **SplitIo** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para habilitar los eventos de e/s divididos en una sesión de registro del kernel de NT, especifique la marca de la **marca de seguimiento de eventos \_ Split de \_ \_ \_ e/s** en el miembro **EnableFlags** de una estructura de [**propiedades de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) al llamar a la función [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

Los consumidores de seguimiento de eventos pueden implementar un procesamiento especial para los eventos de e/s dividida llamando a la función [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) y especificando [**SplitIoGuid**](nt-kernel-logger-constants.md) como parámetro *pGuid* . Use el siguiente tipo de evento para identificar el evento real al consumir eventos.



| Tipo de evento           | Descripción                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valor del tipo de evento, 32 | Evento de e/s dividido. La clase MOF [**SplitIo \_ info**](splitio-info.md) define los datos de evento para este evento. |



 

Los eventos de e/s divididos indican que las solicitudes de e/s se han dividido en varias solicitudes de e/s de disco debido al hardware del disco de creación de reflejo subyacente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 
