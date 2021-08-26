---
description: El filtro Representador null es un representador que descarta cada muestra que recibe, sin mostrar ni representar los datos de ejemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de representador null (Qedit.h)
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
ms.openlocfilehash: 2686c64b3251616ac8cefbe81a77282e5b1a7c6847ef965b6361759118b74756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050885"
---
# <a name="null-renderer-filter"></a>Filtro de representador null

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El filtro Representador null es un representador que descarta cada muestra que recibe, sin mostrar ni representar los datos de ejemplo.



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Tipos de medios de pin de entrada                    | Cualquier tipo de medio                                                                                                       |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Tipos de medios de pin de salida                   | No es aplicable.                                                                                                      |
| Interfaces de pin de salida                    | No es aplicable.                                                                                                      |
| Filtrar CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                    |
| Executable                               | Qedit.dll                                                                                                            |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                  |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Comentarios

Use este filtro cuando un pin de salida en el gráfico requiera una conexión de bajada, pero no desea representar los datos de ese pin. Al conectar el pin de salida al representador null, se completa la conexión sin representar los datos.

Aunque este filtro no representa ninguna muestra, espera el tiempo de presentación de cada muestra antes de descartarla. Por lo tanto, el gráfico se ejecutará a la velocidad normal. Si desea que el gráfico se ejecute lo más rápido posible, establezca el reloj de referencia en **NULL.** Para obtener más información, vea [Setting the Graph Clock](setting-the-graph-clock.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Edición de objetos de servicios](directshow-editing-services-objects.md)
</dt> </dl>

 

 




