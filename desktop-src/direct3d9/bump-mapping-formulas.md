---
description: Direct3D aplica las siguientes fórmulas a los componentes DU y DV en cada píxel del mapa de rugosidad.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Fórmulas de asignación de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153577"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="1936c-103">Fórmulas de asignación de rugosidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1936c-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="1936c-104">Direct3D aplica las siguientes fórmulas a los componentes D<sub>U</sub> y d<sub>V</sub> en cada píxel del mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="1936c-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![fórmulas de transformaciones de matriz de asignación de rugosidad](images/dudv-transform.png)

<span data-ttu-id="1936c-106">En estas fórmulas, las variables D<sub>U</sub> y d<sub>V</sub> se toman directamente de un píxel de mapa de rugosidad y se transforman mediante una matriz de 2x2 para producir los valores Delta de salida D<sub>U</sub>' y d<sub>V</sub>'.</span><span class="sxs-lookup"><span data-stu-id="1936c-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="1936c-107">El sistema utiliza los valores de salida para modificar las coordenadas de textura que abordan el mapa de entorno en la siguiente fase de textura.</span><span class="sxs-lookup"><span data-stu-id="1936c-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="1936c-108">Los coeficientes de la matriz de transformación se establecen a través de los \_ Estados de fase D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 y D3DTSS \_ BUMPENVMAT11 Texture.</span><span class="sxs-lookup"><span data-stu-id="1936c-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="1936c-109">Además de los valores Delta y v, el sistema puede calcular un valor de luminancia que utiliza para modular el color del mapa de entorno en la siguiente fase de mezcla, como se muestra en la siguiente fórmula.</span><span class="sxs-lookup"><span data-stu-id="1936c-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![fórmula para la luminancia de salida, calculada a partir del factor de escala y el desplazamiento](images/l-transform.png)

<span data-ttu-id="1936c-111">En esta fórmula, L ' es la luminancia de salida que se está calculando.</span><span class="sxs-lookup"><span data-stu-id="1936c-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="1936c-112">La variable L es el valor de luminancia tomado de un píxel de mapa de rugosidad, que se multiplica por el factor de escala, S y el desplazamiento por el valor de la variable O. Los \_ Estados de la fase D3DTSS BUMPENVLSCALE y D3DTSS \_ BUMPENVLOFFSET Texture controlan los valores de las variables s y o de la fórmula.</span><span class="sxs-lookup"><span data-stu-id="1936c-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="1936c-113">Esta fórmula solo se aplica cuando la operación de combinación de texturas de la fase que contiene el mapa de rugosidad está establecida en D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="1936c-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="1936c-114">Cuando se usa D3DTOP \_ BUMPENVMAP, el sistema usa un valor de 1,0 para L '.</span><span class="sxs-lookup"><span data-stu-id="1936c-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="1936c-115">Después de calcular los valores Delta de salida D<sub>U</sub>' y d<sub>V</sub>', el sistema los agrega a las coordenadas de textura en la siguiente fase de textura y modula el color elegido por la luminancia para producir el color aplicado al polígono.</span><span class="sxs-lookup"><span data-stu-id="1936c-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1936c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1936c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1936c-117">Asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="1936c-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



