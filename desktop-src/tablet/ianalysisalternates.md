---
description: Contiene una colección de objetos que implementan la interfaz IAnalysisAlternate y que son el resultado del análisis de tinta.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaz IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696548"
---
# <a name="ianalysisalternates-interface"></a>Interfaz IAnalysisAlternates

Contiene una colección de objetos que implementan la interfaz [**IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de tinta.

## <a name="members"></a>Miembros

La interfaz **IAnalysisAlternates** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternates** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAnalysisAlternates** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Recupera el objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Recupera el número de objetos [**IAnalysisAlternate**](ianalysisalternate.md) contenidos en la colección **IAnalysisAlternates** .<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz es equivalente a la clase [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) en el .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternates (método)**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForContextNodes (método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForStrokes (método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

