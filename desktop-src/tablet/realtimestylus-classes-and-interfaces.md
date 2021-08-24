---
description: Esta sección contiene información sobre las interfaces y clases usadas en el lápiz óptico en tiempo real.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Clases e interfaces de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd842219a23accc076ff7fdc8564ccb3ce0c472cb7e26ab036f1048456461f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589955"
---
# <a name="realtimestylus-classes-and-interfaces"></a>Clases e interfaces de RealTimeStylus

Esta sección contiene información sobre las interfaces y clases usadas en el lápiz óptico en tiempo real.

> [!Note]  
> Las interfaces y las clases de lápiz en tiempo real no son compatibles con Automation.

 

## <a name="in-this-section"></a>En esta sección



| Clase                                                      | Descripción                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**RealTimeStylus (clase)**](realtimestylus-class.md)       | Implementa la [**interfaz IRealTimeStylus.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)<br/>                 |
| [**Clase DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))     | Implementa la interfaz [**IDynamicRenderer.**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)<br/>     |
| [**Clase GestureRecognizer**](gesturerecognizer-class.md) | Implementa la [**interfaz IGestureRecognizer.**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)<br/> |
| [**Clase StrokeBuilder**](strokebuilder-class.md)         | Implementa la interfaz [**IStrokeBuilder.**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)<br/>         |



 

## <a name="interfaces"></a>Interfaces



| Interfaz                                                                          | Descripción                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDynamicRenderer (Interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | Expone métodos que permiten controlar la presentación de datos de lápiz óptico en tiempo real a medida que el objeto [**RealTimeStylus Class**](realtimestylus-class.md) controla los datos.<br/> |
| [**IGestureRecognizer (Interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | Expone métodos que permiten reaccionar a eventos mediante el reconocimiento de gestos de lápiz óptico y la posibilidad de agregar datos a la cola de entrada.<br/>                                                  |
| [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | Controla los datos de paquetes de lápiz óptico de un digitalizador en tiempo real.<br/>                                                                                                                    |
| [**IRealTimeStylus2**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | Extiende la interfaz IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | Extiende la interfaz IRealTimeStylus.<br/>                                                                                                                                           |
| [**IRealTimeStylusSynchronization (Interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | Sincroniza el acceso al [**objeto RealTimeStylus Class.**](realtimestylus-class.md)<br/>                                                                                          |
| [**IStrokeBuilder (interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | Expone métodos que permiten crear trazos mediante programación.<br/>                                                                                                              |
| [**IStylusPlugin (interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | Expone métodos que permiten recibir notificaciones de eventos y realizar un procesamiento personalizado basado en esos eventos.<br/>                                                          |
| [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | Representa un complemento asincrónico que se puede agregar a la colección de complementos asincrónicos de la clase [**RealTimeStylus.**](realtimestylus-class.md)<br/>                                |
| [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | Representa un complemento sincrónico que se puede agregar a la colección de complementos sincrónicos [**realTimeStylus Class.**](realtimestylus-class.md)<br/>                                   |



 

## <a name="return-values"></a>Valores devueltos

Los métodos de la biblioteca COM devuelven valores **de HRESULT**. A menos que se indique lo contrario, los significados de **los valores HRESULT** se describen en la tabla siguiente.



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

[Referencia de RealTimeStylus](realtimestylus-reference.md)
</dt> </dl>

 

 
