---
description: Esta sección contiene información sobre las interfaces y las clases utilizadas en el análisis de tinta. Las clases e interfaces de análisis de tinta no son compatibles con la automatización.
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: Clases e interfaces de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539939"
---
# <a name="ink-analysis-classes-and-interfaces"></a>Clases e interfaces de análisis de tinta

Esta sección contiene información sobre las interfaces y las clases utilizadas en el análisis de tinta. Las clases e interfaces de análisis de tinta no son compatibles con la automatización.

## <a name="classes"></a>Clases



| Clase                                    | Descripción                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | Implementa la interfaz [**IAnalysisRegion**](ianalysisregion.md) .<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | Implementa la interfaz [**IInkAnalyzer**](iinkanalyzer.md) .<br/>       |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                                                    | Descripción                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos [**IContextNode**](icontextnode.md) .<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | Contiene una colección de objetos que implementan la interfaz [**IAnalysisAlternate**](ianalysisalternate.md) y que son el resultado del análisis de tinta.<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | Expone métodos y propiedades para una región que representa un área de un documento.<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | Representa el estado de la operación de análisis de tinta al describir si el análisis se completó correctamente y si se produjo alguna advertencia.<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | Representa una advertencia o un error que se produce durante una operación de análisis de tinta.<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | Contiene una colección de objetos que implementan la interfaz [**IAnalysisWarning**](ianalysiswarning.md) y que son el resultado de una operación de análisis de tinta.<br/>                                      |
| [**IContextLink**](icontextlink.md)                         | Representa una relación entre dos objetos [**IContextNode**](icontextnode.md) .<br/>                                                                                                                   |
| [**IContextLinks**](icontextlinks.md)                       | Contiene una colección de objetos que implementan la interfaz [**IContextLink**](icontextlink.md) .<br/>                                                                                                   |
| [**IContextNode**](icontextnode.md)                         | Representa un nodo en un árbol de objetos que se crean como parte del análisis de tinta.<br/>                                                                                                                      |
| [**IContextNodes**](icontextnodes.md)                       | Contiene una colección de objetos que implementan la interfaz [**IContextNode**](icontextnode.md) y que son el resultado de una operación de análisis de tinta.<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | Proporciona acceso a los reconocedores de escritura a mano para su uso con el análisis de tinta.<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | Proporciona acceso al análisis de diseño, la clasificación de escritura y de dibujo y el reconocimiento de escritura a mano.<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | Expone un método para evaluar si un objeto [**IContextNode**](icontextnode.md) cumple o no los criterios especificados.<br/>                                                                              |



 

## <a name="return-values"></a>Valores devueltos

Los métodos de la biblioteca COM de Tablet PC devuelven los valores **HRESULT**. A menos que se indique lo contrario, en esta tabla se describen los significados de los valores **HRESULT** .



| Valor HRESULT                                   | Descripción                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ correcto<br/>                                | Correcto.<br/>                                                                      |
| \_puntero E<br/>                           | Al menos un puntero (para un parámetro de entrada o de salida) no es válido.<br/> |
| E \_ INVALIDARG<br/>                        | El miembro intentó pasar un argumento no válido.<br/>                              |
| \_excepción de entrada manuscrita \_<br/>                    | Se produjo una excepción.<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | El sistema no puede asignar memoria para completar la operación.<br/>                      |
| E \_ FAIL<br/>                              | Se produjo un error no especificado.<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | El miembro intentó usar una operación no válida.<br/>                                 |
| TPC \_ E \_ modo no válido \_<br/>                | El miembro intentó utilizar un modo no válido.<br/>                                      |
| \_ \_ configuración no válida de TPC E \_<br/>       | El miembro intentó usar una configuración no válida.<br/>                             |
| \_Descripción de \_ paquetes no válidos de TPC E \_ \_<br/> | El miembro intentó usar una descripción de paquete no válida.<br/>                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




