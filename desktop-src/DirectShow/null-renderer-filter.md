---
description: El filtro de representador NULL es un representador que descarta cada ejemplo que recibe, sin mostrar ni representar los datos de ejemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de representador nulo (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690609"
---
# <a name="null-renderer-filter"></a>Filtro de representador nulo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El filtro de representador NULL es un representador que descarta cada ejemplo que recibe, sin mostrar ni representar los datos de ejemplo.



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipos de medios de anclaje de entrada                    | Cualquier tipo de medio                                                                                                       |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipos de medios de anclaje de salida                   | No es aplicable.                                                                                                      |
| Interfaces de clavija de salida                    | No es aplicable.                                                                                                      |
| Identificador CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                    |
| Executable                               | Qedit.dll                                                                                                            |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                  |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Observaciones

Use este filtro cuando un PIN de salida en el gráfico requiera una conexión de nivel inferior, pero no desea representar los datos de ese pin. Al conectar el PIN de salida al representador nulo, se completa la conexión sin representar los datos.

Aunque este filtro no representa ningún ejemplo, espera el tiempo de presentación de cada ejemplo antes de descartar el ejemplo. Por lo tanto, el gráfico se ejecutará a la velocidad normal. Si desea que el gráfico se ejecute lo más rápido posible, establezca el reloj de referencia en **null**. Para obtener más información, vea [establecer el reloj del gráfico](setting-the-graph-clock.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de servicios de edición de DirectShow](directshow-editing-services-objects.md)
</dt> </dl>

 

 




