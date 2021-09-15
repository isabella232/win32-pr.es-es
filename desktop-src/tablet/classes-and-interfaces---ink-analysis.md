---
description: Esta sección contiene información sobre las interfaces y clases usadas en el análisis de entrada de lápiz. Las interfaces y las clases de análisis de entrada de lápiz no son compatibles con Automation.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Clases e interfaces de análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468012"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Clases e interfaces de análisis de entrada de lápiz

Esta sección contiene información sobre las interfaces y clases usadas en el análisis de entrada de lápiz. Las interfaces y las clases de análisis de entrada de lápiz no son compatibles con Automation.

## <a name="classes"></a>Clases



| Clase                                    | Descripción                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implementa la [**interfaz IAnalysisRegion.**](ianalysisregion.md)<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implementa la [**interfaz IInkAnalyzer.**](iinkanalyzer.md)<br/>       |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                                                    | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano [**para objetos IContextNode.**](icontextnode.md)<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contiene una colección de objetos que implementan la [**interfaz IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de entrada de lápiz.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Expone métodos y propiedades para una región que representa un área de un documento.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Representa el estado de la operación de análisis de entrada de lápiz mediante la descripción de si el análisis se completó correctamente y si se produjo alguna advertencia.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Representa una advertencia o un error que se produce durante una operación de análisis de entrada de lápiz.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contiene una colección de objetos que implementan la [**interfaz IAnalysisWarning**](ianalysiswarning.md) y que son el resultado de una operación de análisis de entrada de lápiz.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Representa una relación entre dos [**objetos IContextNode.**](icontextnode.md)<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contiene una colección de objetos que implementan la [**interfaz IContextLink.**](icontextlink.md)<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Representa un nodo en un árbol de objetos que se crean como parte del análisis de entrada de lápiz.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contiene una colección de objetos que implementan la [**interfaz IContextNode**](icontextnode.md) y que son el resultado de una operación de análisis de entrada de lápiz.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Proporciona acceso a reconocedores de escritura a mano para su uso con el análisis de entrada de lápiz.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Proporciona acceso al análisis de diseño, la clasificación de escritura y dibujo y el reconocimiento de escritura a mano.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Expone un método para evaluar si un [**objeto IContextNode**](icontextnode.md) cumple o no un criterio especificado.<br/>                                                                              |



 

## <a name="return-values"></a>Valores devueltos

Los métodos de la biblioteca COM de Tablet PC devuelven valores **de HRESULT**. A menos que se indique lo contrario, los significados de los **valores HRESULT** se describen en esta tabla.



| Valor HRESULT                                   | Descripción                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ OK<br/>                                | Correcto.<br/>                                                                      |
| PUNTERO \_ E<br/>                           | Al menos un puntero (para un parámetro de entrada o de salida) no es válido.<br/> |
| E \_ INVALIDARG<br/>                        | El miembro intentó pasar un argumento no válido.<br/>                              |
| E \_ INK \_ EXCEPTION<br/>                    | Se produjo una excepción.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | El sistema no puede asignar memoria para completar la operación.<br/>                      |
| E \_ FAIL<br/>                              | Error no especificado.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | El miembro intentó usar una operación no válida.<br/>                                 |
| TPC \_ E \_ INVALID \_ MODE<br/>                | El miembro intentó usar un modo no válido.<br/>                                      |
| CONFIGURACIÓN NO VÁLIDA DE TPC \_ E \_ \_<br/>       | El miembro intentó usar una configuración no válida.<br/>                             |
| DESCRIPCIÓN DE \_ \_ PAQUETES NO \_ VÁLIDOS DE \_ TPC E<br/> | El miembro intentó usar una descripción de paquete no válida.<br/>                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




