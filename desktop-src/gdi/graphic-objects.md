---
description: El lápiz, el pincel, el mapa de bits, la paleta, la región y la ruta de acceso asociadas a un controlador de dominio se conocen como sus objetos gráficos. Los atributos siguientes están asociados a cada uno de estos objetos.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf256cd8eafd6ee346c12f6658a7c3dd388c94fb4107b010528e47c126fce2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831965"
---
# <a name="graphic-objects"></a>Objetos gráficos

El lápiz, el pincel, el mapa de bits, la paleta, la región y la ruta de acceso asociadas a un controlador de dominio se conocen como sus objetos gráficos. Los atributos siguientes están asociados a cada uno de estos objetos.



| Objeto gráfico | Atributos asociados                                                               |
|----------------|-------------------------------------------------------------------------------------|
| Bitmap         | Size, en bytes; dimensiones, en píxeles; color-format; esquema de compresión; y así sucesivamente. |
| Pincel          | Estilo, color, patrón y origen.                                                  |
| Paleta        | Colores y tamaño (o número de colores).                                              |
| Fuente           | Nombre del tipo, ancho, alto, peso, juego de caracteres, y así sucesivamente.                     |
| Ruta de acceso           | Forma.                                                                              |
| Lápiz            | Estilo, ancho y color.                                                            |
| Region         | Ubicación y dimensiones.                                                            |



 

Cuando una aplicación crea un controlador de dominio, el sistema almacena automáticamente un conjunto de objetos predeterminados en él (no hay ningún mapa de bits o ruta de acceso predeterminado). Una aplicación puede examinar los atributos de los objetos predeterminados llamando a las [**funciones GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**y GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) La aplicación puede cambiar estos valores predeterminados creando un nuevo objeto y seleccionándose en el controlador de dominio. Un objeto se selecciona en un controlador de dominio mediante una llamada a [**la función SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)

Una aplicación puede establecer el color del pincel actual en un valor de color especificado con [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).

La [**función GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) devuelve el color del pincel de controlador de dominio. La [**función SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) establece el color del lápiz en un valor de color especificado. La [**función GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) devuelve el color del lápiz dc.

 

 



