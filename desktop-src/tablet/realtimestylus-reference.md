---
description: Proporciona acceso a los eventos del lápiz óptico que proceden de los digitalizadores táctiles o de lápiz.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referencia de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277779"
---
# <a name="realtimestylus-reference"></a>Referencia de RealTimeStylus

Proporciona acceso a los eventos del lápiz óptico que proceden de los digitalizadores táctiles o de lápiz.

## <a name="in-this-section"></a>En esta sección

-   [Clases e interfaces de RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumeraciones de RealTimeStylus](realtimestylus-enumerations.md)
-   [Estructuras RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Observaciones

Este objeto implementa la interfaz com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Puede controlar por completo, representar, modificar e incluso eliminar datos de la secuencia de paquetes en los complementos sincrónicos y asincrónicos del objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) .

El lápiz en tiempo real proporciona una manera de crear un objeto **InkCollecting** que es de un solo subproceso y que reside en el subproceso de la interfaz de usuario de la aplicación. Este objeto **InkCollecting** obtiene acceso a los datos del lápiz en tiempo real desde la cola. Un objeto **InkCollecting** junto con el lápiz en tiempo real permite la edición de selección en tiempo real y la edición en tiempo real de los datos de tinta recopilados. Para obtener más información, consulte [acceso y manipulación de entradas del lápiz óptico](accessing-and-manipulating-stylus-input.md).

Use el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) para interactuar directamente con el flujo de datos de Tablet Stylus o para bloquear la entrada manuscrita en tiempo real. Use el objeto de [**clase InkCollector**](inkcollector-class.md) , el objeto de [**clase InkOverlay**](inkoverlay-class.md) , el control de [control InkPicture](inkpicture-control-reference.md) o el control de [control InkEdit](inkedit-control-reference.md) cuando el comportamiento predeterminado de estos objetos proporciona el comportamiento que necesita.

Los eventos del lápiz en tiempo real se encuentran en un identificador de ventana específico dentro de un rectángulo de entrada de la ventana específico. RealTimeStylusService puede enviar datos del lápiz óptico a varios objetos de la [**clase RealTimeStylus**](realtimestylus-class.md) . Cada objeto de **clase RealTimeStylus** recibe datos de lápiz óptico para una sección específica de una ventana basada en la [**propiedad IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para ese objeto de la **clase RealTimeStylus** . El objeto de la **clase RealTimeStylus** obtiene los datos del lápiz y, a continuación, los procesa a través de una lista de complementos sincrónicos y asincrónicos.

La diferencia entre los complementos sincrónicos y los complementos asincrónicos se encuentra en el subproceso en el que se ejecutan y en la secuencia de llamada. El subproceso en el que se ejecuta el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) llama a los complementos sincrónicos. Cada vez que se crea una instancia del objeto de la **clase RealTimeStylus** , se crea una instancia de un subproceso de ejecución. Los complementos sincrónicos se ejecutan en este nuevo subproceso con instancias creadas para la instancia del objeto de la **clase RealTimeStylus** . Se llama a los complementos asincrónicos a través de la interfaz de usuario o el subproceso de la aplicación después de que los complementos sincrónicos hayan procesado la secuencia de paquetes y estén almacenadas en la cola de salida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
