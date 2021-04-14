---
description: En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabajar con controladores anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422794"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Trabajar con controladores anteriores (Direct3D 9)

En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.

-   Cuando se trabaja con un dispositivo HAL de T&L, se calcula la intensidad de la niebla pero no se aplica la operación de valor absoluto a este valor. En su lugar, el valor se deja negativo si es lo que se calcula. La mejor manera de evitar esta situación es configurar las transformaciones adecuadamente. Un método menos preferido es hacer que los valores de la niebla-Start y de la niebla-end sean negativos.

Para buscar un controlador de Direct3D 9, busque un valor distinto de cero para D3DDEVCAPS2 \_ STREAMOFFSET en el miembro DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 



