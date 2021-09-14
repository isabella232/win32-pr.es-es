---
description: Modo de ventana de VMR (compatibilidad)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Modo de ventana de VMR (compatibilidad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7312274881642d15b844e0fa950f72e52f92db8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272791"
---
# <a name="vmr-windowed-compatibility-mode"></a>Modo de ventana de VMR (compatibilidad)

VmR está diseñado para ser compatible con todas las aplicaciones de DirectShow existentes. Cuando se usa con una aplicación existente, vmr funciona en modo de ventana con una sola secuencia de vídeo, también denominada modo de compatibilidad. Este modo se proporciona porque VMR-7 es el representador predeterminado en Windows XP y, por tanto, se usa automáticamente en llamadas a métodos de [Intelligent Conectar](intelligent-connect.md) como [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Si la aplicación usa Intelligent Conectar y solo requiere funcionalidades básicas de representación, no necesita ningún código especial para representarse correctamente con VMR-7 en Windows XP.

VMR-9 también se ejecuta en modo de compatibilidad o ventana de forma predeterminada. Sin embargo, VMR-9 nunca es el representador de vídeo predeterminado. Para usar VMR-9 en una aplicación, debe agregarlo explícitamente al gráfico de filtros. Por ese motivo, y dado que el modo sin ventanas proporciona una mejor funcionalidad que el modo con ventanas, no hay ninguna ventaja concreta de usar VMR-9 en modo de compatibilidad o ventana.

**Uso de VMR-7 en modo de compatibilidad o ventana**

No se requiere ninguna programación especial para configurar o controlar VMR-7 en modo de compatibilidad o ventana. Simplemente compile el gráfico de filtro mediante las llamadas estándar de creación de grafos y VMR-7 tendrá como valor predeterminado este modo.

En el modo de compatibilidad o ventana, VMR-7 crea su propia ventana para mostrar el vídeo. Para ello, carga el componente Administrador de ventanas, que expone las interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) [**e IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) La aplicación puede consultar el Administrador de Graph filtros para estas interfaces, exactamente igual que lo haría con el filtro de representador de vídeo antiguo. Para obtener más información, [vea Using Windowed Mode](using-windowed-mode.md).

En la ilustración siguiente se muestra vmr-7 en modo de compatibilidad o ventana.

![vmr en modo de compatibilidad](images/vmr-compat-mode.png)

Para garantizar el nivel máximo de compatibilidad, la ventana de vídeo tiene el mismo nombre de clase que el que creó el antiguo filtro De representador de vídeo y la mayor parte del código del Administrador de ventanas del representador de vídeo antiguo todavía lo usa la máquina virtual. En el modo de compatibilidad o ventana, vmr no consume más recursos del sistema que el representador de vídeo anterior. Dado que VMR-7 solo tiene un flujo de entrada en modo de compatibilidad o ventana, no carga sus componentes mezclador o compositor.

De forma predeterminada, vmr extiende la imagen para rellenar la ventana de vídeo. Para conservar la relación de aspecto del origen, llame al método [**IVMRAspectRatioControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) con la marca \_ VMR ARMODE \_ LETTER \_ BOX.

> [!Note]  
> Las aplicaciones MFC que coloquen la ventana de vídeo en una ventana secundaria deben definir un controlador de mensajes WM ERASEB KGND vacío o el área de visualización del vídeo no volverá a \_ dibujarse correctamente.

 

**Uso de VMR-7 en modo de compatibilidad o ventana con varias Secuencias**

En el modo de compatibilidad o ventana, VMR-7 crea una sola patilla de entrada de forma predeterminada y deshabilita el modo de combinación. Para habilitar el modo de combinación, debe configurar vmr antes de conectarlo. Para obtener más información, vea [VMR con varias Secuencias (modo de combinación).](vmr-with-multiple-streams--mixing-mode.md) En el modo de combinación, vmr carga los componentes de mezcla y compositor, que requieren más recursos del sistema.

**Uso de VMR-9 en modo de ventana**

Dado que VMR-9 no es el representador predeterminado, no tiene un modo de compatibilidad como tal. En su lugar, el valor predeterminado de VMR-9 es el modo de ventana con cuatro pines de entrada. Puede usar este modo para mezclar hasta cuatro secuencias de vídeo. Si necesita mezclar un mayor número de secuencias, debe configurarla como se describe en VMR con varias [Secuencias (modo de combinación).](vmr-with-multiple-streams--mixing-mode.md) De lo contrario, vmr-9 en modo de ventana se comporta exactamente igual que vmr-7 en modo de compatibilidad o ventana.

 

 



