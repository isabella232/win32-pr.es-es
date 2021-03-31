---
description: Expone métodos y propiedades para una región que representa un área de un documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interfaz IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810045"
---
# <a name="ianalysisregion-interface"></a>Interfaz IAnalysisRegion

Expone métodos y propiedades para una región que representa un área de un documento.

## <a name="members"></a>Miembros

La interfaz **IAnalysisRegion** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisRegion** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAnalysisRegion** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](ianalysisregion-clone.md)                           | Crea una copia de **IAnalysisRegion**.<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Restringe el área del **IAnalysisRegion** a la parte de su área que no forma una intersección con el rectángulo especificado.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Restringe el área del **IAnalysisRegion** a la parte de su área que no forma una intersección con el **IAnalysisRegion** especificado.<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Recupera el rectángulo delimitador de **IAnalysisRegion**.<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Recupera una matriz de rectángulos que define el área de **IAnalysisRegion**.<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Restringe el área de este **IAnalysisRegion** al área creada por su intersección con el rectángulo especificado.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Restringe el área de **IAnalysisRegion** al área creada por su intersección con el **IAnalysisRegion** especificado.<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Determina si el área del **IAnalysisRegion** se corta con el rectángulo especificado.<br/>                                     |
| [**Vacío**](ianalysisregion-isempty.md)                       | Recupera un valor que indica si **IAnalysisRegion** representa una región vacía.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Recupera un valor que indica si **IAnalysisRegion** representa una región infinita.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Reduce el **IAnalysisRegion** para representar un área vacía.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Expande el **IAnalysisRegion** para representar un área infinita.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Expande el área de este **IAnalysisRegion** al área creada por su unión con el rectángulo especificado.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Expande el área de este **IAnalysisRegion** al área creada por su unión con el **IAnalysisRegion** especificado.<br/>               |



 

## <a name="remarks"></a>Observaciones

Esta interfaz representa un área que se construye a partir de regiones rectangulares. [**IInkAnalyzer**](iinkanalyzer.md) devuelve o interpreta las coordenadas de un área en el espacio de coordenadas en el que recibe los datos del trazo.

Para obtener los límites actuales del **IAnalysisRegion**, use el método [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) o [**IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).

Para modificar el área de un **IAnalysisRegion** existente, use los métodos siguientes.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**IAnalysisRegion:: ExcludeRegion (método)**](ianalysisregion-excluderegion.md)
-   [**IAnalysisRegion:: IntersectRectangle (método)**](ianalysisregion-intersectrectangle.md)
-   [**IAnalysisRegion:: IntersectRegion (método)**](ianalysisregion-intersectregion.md)
-   [**IAnalysisRegion:: MakeEmpty (método)**](ianalysisregion-makeempty.md)
-   [**IAnalysisRegion:: MakeInfinite (método)**](ianalysisregion-makeinfinite.md)
-   [**IAnalysisRegion:: UnionRectangle (método)**](ianalysisregion-unionrectangle.md)
-   [**IAnalysisRegion:: UnionRegion (método)**](ianalysisregion-unionregion.md)

Esta interfaz es equivalente a la clase System. Windows. Ink. AnalysisCore. AnalysisRegionBase en el .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

