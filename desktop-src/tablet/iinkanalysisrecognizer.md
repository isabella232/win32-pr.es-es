---
description: Proporciona acceso a reconocedores de escritura a mano para su uso con el análisis de entrada de lápiz.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Interfaz IInkAnalysisRecognizer (IACom.h)
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
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350885"
---
# <a name="iinkanalysisrecognizer-interface"></a>IInkAnalysisRecognizer (interfaz)

Proporciona acceso a reconocedores de escritura a mano para su uso con el análisis de entrada de lápiz.

## <a name="members"></a>Miembros

La **interfaz IInkAnalysisRecognizer** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalysisRecognizer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IInkAnalysisRecognizer** tiene estos métodos.



| Método                                                                          | Descripción                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | Recupera las funcionalidades del reconocedor.<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | Recupera el identificador único global (GUID) del reconocedor.<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | Recupera los identificadores de las configuraciones regionales que **admite este IInkAnalysisRecognizer.**<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | Recupera el nombre del reconocedor.<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | Recupera los identificadores únicos globales (GUID) de las propiedades que **admite este IInkAnalysisRecognizer.**<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | Recupera el nombre de proveedor de **IInkAnalysisRecognizer.**<br/>                                                        |



 

## <a name="remarks"></a>Comentarios

Un reconocedor tiene atributos y propiedades específicos que le permiten realizar el reconocimiento. Las propiedades de un reconocedor deben determinarse antes de que se pueda producir el reconocimiento. Los tipos de propiedades que admite un reconocedor determinan los tipos de reconocimiento que puede realizar. Por ejemplo, si un reconocedor no admite escritura a mano cursiva, devuelve resultados inexactos cuando un usuario escribe en cursiva.

Un reconocedor también tiene funcionalidad integrada que administra automáticamente muchos aspectos de la escritura a mano. Por ejemplo, determina las métricas de las líneas en las que se dibujan los trazos. Puede devolver el número de línea de un trazo, pero nunca es necesario especificar cómo se determinan esas métricas de línea debido a la funcionalidad integrada del reconocedor.

[**IInkAnalyzer**](iinkanalyzer.md) mantiene una lista de reconocedores disponibles. Para acceder a esta lista, use el método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority .**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer (Método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

