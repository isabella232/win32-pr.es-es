---
description: Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaz IInkAnalysisRecognizer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696526"
---
# <a name="iinkanalysisrecognizer-interface"></a>Interfaz IInkAnalysisRecognizer

Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.

## <a name="members"></a>Miembros

La interfaz **IInkAnalysisRecognizer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IInkAnalysisRecognizer** tiene estos métodos.



| Método                                                                          | Descripción                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera las capacidades del reconocedor.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Recupera el identificador único global (GUID) del reconocedor.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera los identificadores de las configuraciones regionales admitidas por este **IInkAnalysisRecognizer** .<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera el nombre del reconocedor.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera los identificadores únicos globales (GUID) de las propiedades que admite este **IInkAnalysisRecognizer** .<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera el nombre del proveedor de **IInkAnalysisRecognizer**.<br/>                                                        |



 

## <a name="remarks"></a>Observaciones

Un reconocedor tiene atributos y propiedades específicos que permiten realizar el reconocimiento. Las propiedades de un reconocedor deben determinarse antes de que se pueda realizar el reconocimiento. Los tipos de propiedades que admite un reconocedor determinan los tipos de reconocimiento que puede realizar. Por ejemplo, si un reconocedor no admite la escritura a mano cursiva, devuelve resultados inexactos cuando un usuario escribe en cursiva.

Un reconocedor también tiene una funcionalidad integrada que administra automáticamente muchos aspectos de la escritura a mano. Por ejemplo, determina las métricas de las líneas en las que se dibujan los trazos. Puede devolver el número de línea de un trazo, pero nunca necesita especificar cómo se determinan esas métricas de línea debido a la funcionalidad integrada del reconocedor.

[**IInkAnalyzer**](iinkanalyzer.md) mantiene una lista de los reconocedores disponibles. Para tener acceso a esta lista, use el método [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer:: CreateCustomRecognizer (método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

