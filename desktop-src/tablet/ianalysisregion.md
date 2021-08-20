---
description: Expone métodos y propiedades para una región que representa un área de un documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interfaz IAnalysisRegion (IACom.h)
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
ms.openlocfilehash: d8dc5b0af5746328ead68be3896148b7a4ddf79d6844a6d4ae976b2f29592d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045069"
---
# <a name="ianalysisregion-interface"></a>Interfaz IAnalysisRegion

Expone métodos y propiedades para una región que representa un área de un documento.

## <a name="members"></a>Miembros

La **interfaz IAnalysisRegion** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisRegion** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAnalysisRegion** tiene estos métodos.



| Método                                                           | Descripción                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](ianalysisregion-clone.md)                           | Crea una copia de **IAnalysisRegion.**<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Restringe el área de **IAnalysisRegion** a la parte de su área que no forma una intersección con el rectángulo especificado.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Restringe el área de **IAnalysisRegion** a la parte de su área que no forma una intersección con el **objeto IAnalysisRegion especificado.**<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Recupera el rectángulo delimitador de **IAnalysisRegion.**<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Recupera una matriz de rectángulos que define el área de **IAnalysisRegion**.<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Restringe el área de esta **IAnalysisRegion** al área creada por su intersección con el rectángulo especificado.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Restringe el área de **IAnalysisRegion** al área creada por su intersección con la **región IAnalysisRegion especificada.**<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Determina si el área de **IAnalysisRegion** forma una intersección con el rectángulo especificado.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Recupera un valor que indica si **IAnalysisRegion** representa una región vacía.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Recupera un valor que indica si **IAnalysisRegion** representa una región infinita.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Reduce **IAnalysisRegion para** representar un área vacía.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Expande **IAnalysisRegion para** representar un área infinita.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Expande el área de **esta IAnalysisRegion** al área creada por su unión con el rectángulo especificado.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Expande el área de **esta IAnalysisRegion** al área creada por su unión con la **región IAnalysisRegion especificada.**<br/>               |



 

## <a name="remarks"></a>Comentarios

Esta interfaz representa un área que se construye a partir de regiones rectangulares. [**IInkAnalyzer**](iinkanalyzer.md) devuelve o interpreta las coordenadas de un área dentro del espacio de coordenadas en el que recibe datos de trazo.

Para obtener los límites actuales de **IAnalysisRegion,** use el método [**IAnalysisRegion::GetBounds**](ianalysisregion-getbounds.md) o el método [**IAnalysisRegion::GetRegionScans**](ianalysisregion-getregionscans.md).

Para modificar el área de una **IAnalysisRegion** existente, use los métodos siguientes.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**IAnalysisRegion::ExcludeRegion (Método)**](ianalysisregion-excluderegion.md)
-   [**IAnalysisRegion::IntersectRectangle (Método)**](ianalysisregion-intersectrectangle.md)
-   [**IAnalysisRegion::IntersectRegion (Método)**](ianalysisregion-intersectregion.md)
-   [**IAnalysisRegion::MakeEmpty (Método)**](ianalysisregion-makeempty.md)
-   [**IAnalysisRegion::MakeInfinite (Método)**](ianalysisregion-makeinfinite.md)
-   [**IAnalysisRegion::UnionRectangle (Método)**](ianalysisregion-unionrectangle.md)
-   [**IAnalysisRegion::UnionRegion (Método)**](ianalysisregion-unionregion.md)

Esta interfaz es equivalente al sistema. Windows. Clase Ink.AnalysisCore.AnalysisRegionBase del .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

