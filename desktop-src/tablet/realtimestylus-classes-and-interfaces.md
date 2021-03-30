---
description: Esta sección contiene información sobre las interfaces y las clases que se usan en el lápiz óptico en tiempo real.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Clases e interfaces de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910750"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Clases e interfaces de RealTimeStylus

Esta sección contiene información sobre las interfaces y las clases que se usan en el lápiz óptico en tiempo real.

> [!Note]  
> Las clases e interfaces del lápiz óptico en tiempo real no son compatibles con la automatización.

 

## <a name="in-this-section"></a>En esta sección



| Clase                                                      | Descripción                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus (clase)**](realtimestylus-class.md)       | Implementa la interfaz [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .<br/>                 |
| [**DynamicRenderer (clase)**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementa la interfaz de la [**interfaz IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .<br/>     |
| [**Clase GestureRecognizer**](gesturerecognizer-class.md) | Implementa la interfaz de la [**interfaz IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .<br/> |
| [**Clase StrokeBuilder**](strokebuilder-class.md)         | Implementa la interfaz de la [**interfaz IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .<br/>         |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                                                                          | Descripción                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Expone métodos que permiten controlar la presentación de los datos del lápiz óptico en tiempo real, ya que el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) controla los datos.<br/> |
| [**Interfaz IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Expone métodos que permiten reaccionar a los eventos mediante el reconocimiento de los gestos del lápiz óptico y le permite agregar datos a la cola de entrada.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Controla los datos del paquete de lápiz óptico desde un digitalizador en tiempo real.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Extiende la interfaz IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Extiende la interfaz IRealTimeStylus.<br/>                                                                                                                                           |
| [**Interfaz IRealTimeStylusSynchronization**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Sincroniza el acceso al objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) .<br/>                                                                                          |
| [**Interfaz IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Expone métodos que permiten crear trazos mediante programación.<br/>                                                                                                              |
| [**Interfaz IStylusPlugin**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Expone métodos que permiten recibir notificaciones de eventos y realizar un procesamiento personalizado basado en esos eventos.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Representa un complemento asincrónico que se puede Agregar a la colección de complementos asincrónicos de la [**clase RealTimeStylus**](realtimestylus-class.md) .<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Representa un complemento sincrónico que se puede Agregar a la colección de complementos sincrónicos de la [**clase RealTimeStylus**](realtimestylus-class.md) .<br/>                                   |



 

## <a name="return-values"></a>Valores devueltos

Los métodos de la biblioteca COM devuelven los valores **HRESULT**. A menos que se indique lo contrario, los significados de los valores **HRESULT** se describen en la tabla siguiente.



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

[Referencia de RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
