---
description: Proporciona acceso a los eventos del lápiz procedentes de digitalizadores táctiles o de lápiz.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referencia de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05518658a7bca01090e72cbe68d23b98d5ffffed14b2d8d091fa8c884e9f7c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091465"
---
# <a name="realtimestylus-reference"></a>Referencia de RealTimeStylus

Proporciona acceso a los eventos del lápiz procedentes de digitalizadores táctiles o de lápiz.

## <a name="in-this-section"></a>En esta sección

-   [Clases e interfaces de RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumeraciones RealTimeStylus](realtimestylus-enumerations.md)
-   [Estructuras de RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Comentarios

Este objeto implementa la [**interfaz COM IRealTimeStylus.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Puede controlar completamente, representar dinámicamente, modificar e incluso eliminar datos de la secuencia de paquetes dentro de los complementos sincrónicos y asincrónicos del objeto [**RealTimeStylus Class.**](realtimestylus-class.md)

El lápiz óptico en tiempo real proporciona una manera de crear un objeto **InkCollecting** de un solo subproceso y que residen en el subproceso de interfaz de usuario de la aplicación. Este **objeto InkCollecting** accede a los datos del lápiz óptico en tiempo real de la cola. Un **objeto InkCollecting** junto con el lápiz óptico en tiempo real permite la edición de la selección en tiempo real y la edición en tiempo real de los datos de lápiz recopilados. Para obtener más información, vea [Acceso y manipulación de entrada de lápiz óptico.](accessing-and-manipulating-stylus-input.md)

Use el [**objeto RealTimeStylus Class**](realtimestylus-class.md) para interactuar directamente con el flujo de datos del lápiz óptico de tableta o para bloquear la entrada en tiempo real. Use el objeto [**InkCollector Class,**](inkcollector-class.md) el objeto [**InkOverlay Class,**](inkoverlay-class.md) el [control Control InkPicture](inkpicture-control-reference.md) o el [control InkEdit cuando](inkedit-control-reference.md) el comportamiento predeterminado de estos objetos proporciona el comportamiento que necesita.

Los eventos de lápiz óptico en tiempo real se encuentran en un identificador de ventana específico dentro de un rectángulo de entrada de ventana específico. RealTimeStylusService puede enviar datos de lápiz óptico a varios objetos de la clase [**RealTimeStylus.**](realtimestylus-class.md) Cada objeto **RealTimeStylus Class** recibe datos de lápiz óptico para una sección específica de una ventana basada en la propiedad [**IRealTimeStylus::WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para ese objeto **realTimeStylus Class.** El **objeto RealTimeStylus Class** obtiene los datos del lápiz óptico y, a continuación, lo procesa a través de una lista de complementos sincrónicos y asincrónicos.

La diferencia entre los complementos sincrónicos y los complementos asincrónicos reside en el subproceso en el que se ejecutan y en la secuencia de llamada. El subproceso en el que se ejecuta el objeto [**RealTimeStylus Class**](realtimestylus-class.md) llama a los complementos sincrónicos. Cada vez que se crea una instancia del objeto de clase **RealTimeStylus,** se crea una instancia de un subproceso de ejecución. Los complementos sincrónicos se ejecutan en este nuevo subproceso del que se crea una instancia para la instancia del objeto **RealTimeStylus Class.** Los complementos asincrónicos se llaman a través de la interfaz de usuario o el subproceso de aplicación después de que los complementos sincrónicos hayan procesado la secuencia de paquetes y se haya almacenado en la cola de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDynamicRenderer (Interfaz)**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
