---
title: DirectComposition
description: En este tema se explica el propósito de Microsoft DirectComposition, se identifican sus requisitos en tiempo de ejecución y se describe el fondo de programación que se necesita para usar Microsoft DirectComposition de forma eficaz.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985415"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Propósito

Microsoft DirectComposition es un componente Windows que permite la composición de mapas de bits de alto rendimiento con transformaciones, efectos y animaciones. Los desarrolladores de aplicaciones pueden usar la API DirectComposition para crear interfaces de usuario visualmente atractivas y que ofrezcan transiciones animadas fluidas y enriquecidas, de un objeto visual a otro.

DirectComposition permite transiciones enriquecciones y fluidas al lograr una alta velocidad de fotogramas, usar hardware gráfico y funcionar independientemente del subproceso de interfaz de usuario. DirectComposition puede aceptar contenido de mapa de bits dibujado por diferentes bibliotecas de representación, incluidos los mapas de bits de Microsoft DirectX y los mapas de bits representados en una ventana (mapas de bits HWND). Además, DirectComposition admite diversas transformaciones, como transformaciones afín 2D y transformaciones de perspectiva 3D, así como efectos básicos como recorte y opacidad.

DirectComposition está diseñado para simplificar el proceso de composición de [*objetos visuales*](directcomposition-glossary.md) y creación de transiciones animadas. Si la aplicación ya contiene código de representación o ya usa la API de DirectX recomendada, solo debe realizar una cantidad mínima de trabajo para usar DirectComposition de forma eficaz.

## <a name="developer-audience"></a>Audiencia de desarrolladores

DirectComposition API está pensada para desarrolladores de gráficos experimentados y altamente capaces que conocen C/C++, tienen una sólida comprensión del modelo de objetos componentes (COM) y están familiarizados con los conceptos de programación de Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

DirectComposition se introdujo en Windows 8. Se incluye en plataformas arm de 32 bits, de 64 bits.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [¿Por qué usar DirectComposition?](why-use-directcomposition-.md)<br/>     | En este tema se describen las funcionalidades y ventajas de DirectComposition. <br/>                                                                           |
| [Uso de DirectComposition](how-to-use-directcomposition.md)<br/> | En esta sección se describen los procedimientos recomendados para usar DirectComposition API y se muestra cómo usar la API para realizar varias tareas comunes. <br/> |
| [Conceptos de DirectComposition](directcomposition-concepts.md)<br/>     | En esta sección se proporciona información general conceptual de DirectComposition.<br/>                                                                                   |
| [Referencia de DirectComposition](reference.md)<br/>                     | En esta sección se proporciona información de referencia detallada de los elementos que integran directComposition API.<br/>                                       |
| [Ejemplos de DirectComposition](directcomposition-code-samples.md)<br/>  | En las siguientes aplicaciones de ejemplo se muestra cómo usar DirectComposition API y cómo demostrar sus funcionalidades. <br/>                                      |
| [Glosario de DirectComposition](directcomposition-glossary.md)<br/>     | En este tema se definen los términos de DirectComposition. <br/>                                                                                                        |



 

 

 





