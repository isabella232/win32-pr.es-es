---
description: En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabajar con controladores anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24284c706d49ce3294e23486f72150ffd74ee376e2be0d7d06dca09877eb7cc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796914"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Trabajar con controladores anteriores (Direct3D 9)

En esta sección se enumeran los problemas que se pueden encontrar al trabajar con Direct3D 9 en controladores escritos para versiones de Direct3D anteriores a Direct3D 9.

-   Al trabajar con un dispositivo T&L LO, se calcula la intensidad de la columna, pero la operación de valor absoluto no se aplica a este valor. En su lugar, el valor se deja negativo si es lo que se calcula. La mejor manera de evitar esta situación es configurar las transformaciones correctamente. Un método menos preferido consiste en hacer que los valores de start-end y de extremo a extremo sea negativo para que coincidan.

Para buscar un controlador Direct3D 9, busque un valor distinto de cero para D3DDEVCAPS2 STREAMOFFSET en el miembro \_ DevCaps2 de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 



