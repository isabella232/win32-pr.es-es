---
description: Contiene una colección de objetos que implementan la interfaz IAnalysisAlternate y que son el resultado del análisis de entrada de lápiz.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaz IAnalysisAlternates (IACom.h)
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
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058095"
---
# <a name="ianalysisalternates-interface"></a>IAnalysisAlternates (interfaz)

Contiene una colección de objetos que implementan la [**interfaz IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de entrada de lápiz.

## <a name="members"></a>Miembros

La **interfaz IAnalysisAlternates** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisAlternates** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAnalysisAlternates** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Recupera el [**objeto IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado dentro de la colección.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Recupera el número de [**objetos IAnalysisAlternate**](ianalysisalternate.md) contenidos en la **colección IAnalysisAlternates.**<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz es equivalente a [**System.Windows. Clase Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) del .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternates (Método)**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForContextNodes (Método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer::GetAlternatesForStrokes (Método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

