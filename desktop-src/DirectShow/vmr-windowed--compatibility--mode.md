---
description: Modo de ventana de VMR (compatibilidad)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modo de ventana de VMR (compatibilidad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571680"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modo de ventana de VMR (compatibilidad)

VMR está diseñado para ser compatible con todas las aplicaciones de DirectShow existentes. Cuando se usa con una aplicación existente, VMR funciona en modo de ventana con un solo flujo de vídeo, también denominado modo de compatibilidad. Este modo se proporciona porque VMR-7 es el representador predeterminado en Windows XP y, por lo tanto, se usa automáticamente en llamadas a métodos de [conexión inteligentes](intelligent-connect.md) como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Si la aplicación usa conexión inteligente y solo requiere capacidades de representación básicas, no es necesario que el código especial se represente correctamente con VMR-7 en Windows XP.

VMR-9 también se ejecuta en modo de ventana/compatibilidad de forma predeterminada. Sin embargo, VMR-9 nunca es el representador de vídeo predeterminado. Para usar VMR-9 en una aplicación, debe agregarla explícitamente al gráfico de filtro. Por ese motivo, y dado que el modo sin ventanas proporciona una mejor funcionalidad que el modo de ventana, no hay ninguna ventaja especial en el uso de VMR-9 en el modo de compatibilidad con ventanas.

**Usar la VMR-7 en el modo de compatibilidad con ventanas**

No es necesaria ninguna programación especial para configurar o controlar el modelo VMR-7 en modo de compatibilidad con ventanas. Basta con compilar el gráfico de filtro mediante las llamadas estándar de generación de gráficos y el valor de VMR-7 se establecerá de forma predeterminada en este modo.

En el modo de compatibilidad con ventanas, VMR-7 crea su propia ventana para mostrar el vídeo. Para ello, carga el componente de administrador de ventanas, que expone las interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . La aplicación puede consultar el administrador de gráficos de filtro para estas interfaces, exactamente como lo haría con el filtro de representador de vídeo anterior. Para obtener más información, vea [usar el modo de ventana](using-windowed-mode.md).

En la ilustración siguiente se muestra la imagen VMR-7 en modo de compatibilidad con ventanas.

![VMR en modo de compatibilidad](images/vmr-compat-mode.png)

Para garantizar el máximo nivel de compatibilidad, la ventana de vídeo tiene el mismo nombre de clase que la creada por el filtro de representador de vídeo anterior y la mayor parte del código del administrador de ventanas del representador de vídeo anterior todavía se usa en la VMR. En el modo de compatibilidad con ventanas, el VMR no consume más recursos del sistema que el anterior representador de vídeo. Dado que VMR-7 solo tiene un flujo de entrada en modo de ventana/compatibilidad, no carga sus componentes de mezclador o compositor.

De forma predeterminada, la VMR amplía la imagen para rellenar la ventana de vídeo. Para conservar la relación de aspecto del origen, llame al método [**IVMRAspectRatioControl:: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) con la marca de cuadro de letra de VMR \_ ARMODE \_ \_ .

> [!Note]  
> Las aplicaciones MFC que colocan la ventana de vídeo en una ventana secundaria deben definir un controlador de mensajes ERASEBKGND de WM vacío \_ , o el área de presentación de vídeo no volverá a dibujarse correctamente.

 

**Usar VMR-7 en modo de ventana/compatibilidad con varias secuencias**

En el modo de compatibilidad/ventanas, el VMR-7 crea un solo PIN de entrada de forma predeterminada y deshabilita el modo de combinación. Para habilitar el modo de combinación, debe configurar el VMR antes de conectarlo. Para obtener más información, consulte [VMR con varias secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md). En el modo de combinación, VMR carga los componentes de mezcla y compositor, que requieren más recursos del sistema.

**Usar VMR-9 en modo de ventana**

Dado que VMR-9 no es el representador predeterminado, no tiene un modo de compatibilidad como tal. En su lugar, el valor predeterminado de VMR-9 es el modo de ventana con cuatro clavijas de entrada. Puede usar este modo para mezclar hasta cuatro secuencias de vídeo. Si necesita mezclar un número mayor de secuencias, debe configurarla como se describe en [VMR con varias secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md). De lo contrario, el modelo VMR-9 en modo de ventana se comporta exactamente igual que VMR-7 en modo de compatibilidad con ventanas.

 

 



