---
title: DirectComposition
description: En este tema se explica el propósito de Microsoft DirectComposition, se identifican los requisitos de tiempo de ejecución y se describe el fondo de programación que necesita para usar Microsoft DirectComposition de forma eficaz.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API de DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356898"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Propósito

Microsoft DirectComposition es un componente de Windows que permite la composición de mapas de bits de alto rendimiento con transformaciones, efectos y animaciones. Los desarrolladores de aplicaciones pueden usar la API DirectComposition para crear interfaces de usuario visualmente atractivas y que ofrezcan transiciones animadas fluidas y enriquecidas, de un objeto visual a otro.

DirectComposition permite transiciones enriquecidas y fluidas al conseguir una velocidad de fotogramas alta, usar hardware de gráficos y trabajar independientemente del subproceso de interfaz de usuario. DirectComposition puede aceptar el contenido del mapa de bits dibujado por diferentes bibliotecas de representación, incluidos los mapas de bits de Microsoft DirectX, y los mapas de bits representados en una ventana (mapas de bits HWND). Además, DirectComposition admite una variedad de transformaciones, como transformaciones afines de 2D y transformaciones de perspectiva 3D, así como efectos básicos como el recorte y la opacidad.

DirectComposition está diseñado para simplificar el proceso de composición de [*objetos visuales*](directcomposition-glossary.md) y la creación de transiciones animadas. Si su aplicación ya contiene código de representación o ya usa la API de DirectX recomendada, solo tiene que realizar una cantidad mínima de trabajo para usar DirectComposition de forma eficaz.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de DirectComposition está destinada a desarrolladores de gráficos experimentados y altamente compatibles que saben C/C++, tienen una comprensión sólida del modelo de objetos componentes (COM) y están familiarizados con los conceptos de programación de Windows.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

DirectComposition se presentó en Windows 8. Se incluye en plataformas de 32 bits, 64 bits y ARM.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                       | Descripción                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [¿Por qué usar DirectComposition?](why-use-directcomposition-.md)<br/>     | En este tema se describen las capacidades y ventajas de DirectComposition. <br/>                                                                           |
| [Cómo usar DirectComposition](how-to-use-directcomposition.md)<br/> | En esta sección se describen los procedimientos recomendados para usar la API de DirectComposition y se muestra cómo usar la API para realizar varias tareas comunes. <br/> |
| [Conceptos de DirectComposition](directcomposition-concepts.md)<br/>     | En esta sección se proporciona información general conceptual de DirectComposition.<br/>                                                                                   |
| [Referencia de DirectComposition](reference.md)<br/>                     | En esta sección se proporciona información de referencia detallada para los elementos que componen la API de DirectComposition.<br/>                                       |
| [Ejemplos de DirectComposition](directcomposition-code-samples.md)<br/>  | Las aplicaciones de ejemplo siguientes muestran cómo usar la API de DirectComposition y demostrar sus capacidades. <br/>                                      |
| [Glosario DirectComposition](directcomposition-glossary.md)<br/>     | En este tema se definen los términos de DirectComposition. <br/>                                                                                                        |



 

 

 





