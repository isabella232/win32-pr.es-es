---
title: Prácticas recomendadas para DirectComposition
description: En este tema se describen los procedimientos recomendados para usar Microsoft DirectComposition.
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- prácticas recomendadas para DirectComposition
- prácticas recomendadas para DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793575"
---
# <a name="best-practices-for-directcomposition"></a>Prácticas recomendadas para DirectComposition

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los procedimientos recomendados para usar Microsoft DirectComposition.

-   [procedimientos recomendados](#best-practices-for-directcomposition)
-   [Consideraciones de seguridad](#security-considerations)
-   [Temas relacionados](#related-topics)

## <a name="best-practices"></a>Procedimientos recomendados

En la tabla siguiente se presentan las prácticas recomendadas para trabajar con objetos visuales de Microsoft DirectComposition.



| Práctica                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Después de crear un dispositivo DirectComposition, llame al método [**IDCompositionDevice:: CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) en respuesta a cada mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) para asegurarse de que el dispositivo todavía es válido.<br/> | Si se pierde el dispositivo de infraestructura de gráficos de Microsoft DirectX (DXGI), también se pierde el dispositivo DirectComposition asociado con el dispositivo DXGI. Cuando detecta un dispositivo perdido, DirectComposition envía el mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) a todas las ventanas. Llamar a [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) en respuesta a cada mensaje de **\_ Paint de WM** le permite determinar si el objeto de dispositivo DirectComposition sigue siendo válido y, si no es así, realizar los pasos necesarios para recuperar el contenido. <br/> Para obtener más información, consulte [Device Object](basic-concepts.md).<br/> |
| Cree solo el número de objetos visuales necesarios para una composición o animación y destruya los objetos visuales inmediatamente después de que DirectComposition termine de usarlos.<br/>                                                                                            | DirectComposition usa la unidad de procesamiento de gráficos (GPU), un recurso que la aplicación comparte con otras aplicaciones y el sistema operativo. Esta práctica garantiza que todas las aplicaciones y el sistema operativo reciban los recursos de GPU necesarios.<br/> Para obtener más información, consulte [objetos visuales](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                     |
| No oculte los objetos visuales estableciendo la opacidad en 0%; en su lugar, quite los objetos visuales del árbol visual.<br/>                                                                                                                                                          | Establecer la opacidad en 0% requiere más recursos del sistema que quitarlos del árbol visual.<br/> Para obtener más información, vea [opacidad](effects.md) y [árbol visual](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| No oculte un visual aplicando un rectángulo de recorte vacío (con tamaño cero) a un valor visual. En su lugar, quite el visual del árbol visual. <br/>                                                                                                                 | Quitar un objetos visuales del árbol visual da como resultado un mejor rendimiento que aplicar un rectángulo de recorte vacío.<br/> Para obtener más información, vea [recorte](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| No aplique un rectángulo de recorte a un visual si el rectángulo de recorte no es necesario, como un rectángulo de recorte que incluye todo el contenido del mapa de bits del visual.<br/>                                                                                       | Los rectángulos de recorte innecesarios perjudican el rendimiento del sistema.<br/> Para obtener más información, vea [recorte](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Si necesita un mapa de bits grande de un solo color, cree una superficie de mapa de bits más pequeña y, a continuación, aplique una transformación de escala en lugar de crear una superficie de tamaño completo. <br/>                                                                                                | Aplicar una transformación de escala a una superficie menor utiliza menos recursos del sistema que una superficie de tamaño completo.<br/> Para obtener más información, vea [objetos de mapa de bits](bitmap-surfaces.md) y [transformaciones](transforms.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| Evite aplicar transformaciones 3D a varios niveles de un árbol visual, como a un elemento primario y a sus descendientes. <br/>                                                                                                                                        | Aplicar transformaciones 3D a varios niveles de un árbol visual puede producir resultados imprevistos porque las transformaciones 3D no se multiplican en el árbol. Por ejemplo, un giro de 90 grados alrededor del eje y de un elemento secundario, y un giro de 90 grados alrededor del eje y de un elemento primario, hace que ambos objetos visuales se roten en nada.<br/> Para obtener más información, consulte [Effects](effects.md) (Efectos).<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

En los artículos siguientes se proporcionan instrucciones para escribir código de C++ seguro.

-   [Prácticas recomendadas de seguridad para C++](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [Patterns & prácticas guía de seguridad para aplicaciones](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar DirectComposition](how-to-use-directcomposition.md)
</dt> </dl>

 

