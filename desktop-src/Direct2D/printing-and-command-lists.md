---
title: Impresión y listas de comandos
description: El control Direct2D \ 32;print es un nuevo componente del módulo Direct2D de Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162634"
---
# <a name="printing-and-command-lists"></a>Impresión y listas de comandos

El control de impresión [**de**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) [Direct2D](./direct2d-portal.md) es un nuevo componente del módulo Direct2D de Windows 8. Este componente permite que las aplicaciones de Direct2D reutilicen sus llamadas de dibujo de Direct2D (en términos de cambios de estado y primitivas de destino) para entregar resultados de impresión similares a los que se ven en la pantalla.

La interfaz [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) representa un trabajo de impresión virtual: puede crear un control de impresión [direct2D](./direct2d-portal.md) para iniciar un nuevo trabajo de impresión, pasar contenido de Direct2D para cada página que quiera imprimir y, a continuación, cerrar el control de impresión para completar un trabajo de impresión.

> [!Note]  
> Un control de impresión se asigna a un único trabajo de impresión, y no se puede reutilizar.

El control de impresión de [Direct2D](./direct2d-portal.md) convierte y optimiza el pasado en el contenido de Direct2D para el subs sistema de impresión, que funciona con las impresoras reales para entregar la impresión real. Todos los detalles específicos de impresión se ocultan en las aplicaciones de Direct2D, lo que significa que las aplicaciones de Direct2D se pueden imprimir sin saber a qué dispositivos están dibujando ni cómo se traducen los dibujos a la impresión.

Para imprimir con [Direct2D,](./direct2d-portal.md)debe preparar una lista de comandos de Direct2D para cada página que quiera imprimir y, a continuación, pasar esa lista de comandos al control de impresión de Direct2D. Para preparar esa lista de comandos de Direct2D, basta con crear y establecer una lista de comandos como destino de dibujo del contexto del dispositivo actual y, a continuación, dibujar en ese contexto de dispositivo, exactamente como si se dibujara en un destino de mapa de bits para su presentación. Consulte [Devices and Device Contexts (Dispositivos y contextos de dispositivo)](devices-and-device-contexts.md) para obtener más información sobre los dispositivos y destinos.

En el diagrama siguiente se muestra la interacción entre la aplicación, el contexto del dispositivo, el destino de mapa de bits, el destino de la lista de comandos y el control de impresión.

> [!Note]  
> Los Windows de Sub-System de impresión y de impresora están en gris porque están completamente ocultos en [las aplicaciones de Direct2D.](./direct2d-portal.md)

![diagrama que muestra cómo interactúan la lista de comandos y la impresión con una aplicación y direct2d.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Ejemplo

El proceso completo de impresión de contenido de Direct2D incluye los pasos siguientes.

1.  Cree un control de impresión para iniciar un trabajo de impresión.
2.  Agregue una página al control de impresión pasando una lista de comandos.
3.  Repita el paso 2 para cada página del resto del documento.
4.  Cierre el control de impresión para completar el trabajo de impresión.

Este es un ejemplo de código que muestra el proceso.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Temas relacionados

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Mejora del rendimiento de las aplicaciones e impresión de Direct2D](improving-direct2d-performance.md)