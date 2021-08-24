---
description: El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fuente OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18324f3a9c84553da81c9f9723a2ecd67c03539b4dd39c7a80afc4be5cdcda66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147098"
---
# <a name="opentype-font-format"></a>Formato de fuente OpenType

El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType. Las fuentes OpenType permiten la asignación entre caracteres y [glifos,](uniscribe-glossary.md)lo que permite la compatibilidad con ligaduras, formas posicionales, alternativas y otras sustituciones. Las fuentes OpenType también pueden incluir información que admite el posicionamiento de glifo bidimensional y los datos adjuntos de glifo, y pueden contener trueType o PostScript contornos.

Las características de diseño de las fuentes OpenType se organizan por scripts y lenguajes, lo que permite que una sola fuente admita varios sistemas de escritura, incluso dentro del mismo script. Para garantizar la coherencia en las operaciones de diseño de texto y evitar sobrecargas innecesarias en archivos de fuentes o aplicaciones, muchos de los algoritmos semánticos de lenguaje y diseño de texto se incluyen en Uniscribe. Esto libera al desarrollador de fuentes de tener que definir reglas de script generalizadas dentro de una fuente.

Las aplicaciones pueden introducir conocimientos o preferencias específicos relacionados con el diseño de scripts. Las fuentes de diseño OpenType pueden incluso contener reglas de diseño que duplican o reemplazan a las aplicadas por los servicios del sistema operativo. La estructura en capas de los servicios de sistema operativo que admiten el diseño de texto permite a una aplicación elegir la información de diseño que se va a usar y seleccionar cómo aplicarla. Para obtener más información, consulte la información general sobre las especificaciones [de tipografía de Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la [especificación OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



