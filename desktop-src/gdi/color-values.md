---
description: El color se define como una combinación de tres colores primarios, rojo, verde y azul.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valores de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155656"
---
# <a name="color-values"></a>Valores de color

El color se define como una combinación de tres colores primarios, rojo, verde y azul. el sistema identifica un color asignándole un valor de color (a veces denominado tripledo RGB), que consta de valores de 3 8 bits que especifican las intensidades de sus componentes de color. Black tiene la intensidad mínima para rojo, verde y azul, por lo que el valor de color para Black es (0, 0,0). Blanco tiene la intensidad máxima de rojo, verde y azul, por lo que su valor de color es (255, 255, 255).

> [!Note]  
> Si la coincidencia de color de imagen está habilitada, la definición de color y el significado de un valor de color depende del tipo de espacio de colores que está establecido actualmente para el contexto de dispositivo.

 

El sistema y las aplicaciones usan parámetros y variables que tienen el tipo [COLORREF](colorref.md) para pasar y almacenar los valores de color. Por ejemplo, la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica el color de cada lápiz estableciendo el miembro **lopnColor** de una estructura [**logpen (**](/windows/win32/api/wingdi/ns-wingdi-logpen) en un valor de color. Las aplicaciones pueden extraer los valores individuales de los componentes rojo, verde y azul de un valor de color mediante el uso de las macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)y [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente. Las aplicaciones pueden crear un valor de color a partir de valores de componentes individuales mediante la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) . Al crear o examinar una paleta lógica, una aplicación utiliza la estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para definir los valores de color y para examinar los valores de los componentes individuales.

 

 



