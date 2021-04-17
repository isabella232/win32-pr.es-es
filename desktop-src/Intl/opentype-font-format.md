---
description: El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato de fuente OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653065"
---
# <a name="opentype-font-format"></a>Formato de fuente OpenType

El formato de fuente OpenType basado en Unicode amplía el formato de archivo de fuente TrueType. Las fuentes OpenType permiten la asignación entre caracteres y [glifos](uniscribe-glossary.md), habilitando la compatibilidad con ligaduras, formatos posicionales, alternativas y otras sustituciones. Las fuentes OpenType también pueden incluir información que admite la posición de glifos bidimensionales y los datos adjuntos del glifo, y pueden contener contornos TrueType o PostScript.

Las características de diseño dentro de las fuentes OpenType se organizan por scripts y lenguajes, lo que permite que una sola fuente admita varios sistemas de escritura, incluso dentro del mismo script. Para garantizar la coherencia en las operaciones de diseño de texto y evitar una sobrecarga innecesaria en archivos o aplicaciones de fuentes, muchos de los algoritmos de diseño de texto y semánticos del lenguaje se incluyen en Uniscribe. Esto evita que el desarrollador de fuentes tenga que definir reglas de script generalizadas dentro de una fuente.

Las aplicaciones pueden introducir información o preferencias específicas en relación con el diseño del script. Las fuentes de diseño OpenType pueden incluir incluso reglas de diseño que dupliquen o reemplacen a las aplicadas por los servicios del sistema operativo. La estructura en capas de los servicios del sistema operativo que admiten el diseño de texto permite a una aplicación elegir la información de diseño que se va a utilizar y seleccionar cómo aplicarla. Para obtener más información, vea información [General sobre las especificaciones tipográficas de Microsoft](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la [especificación OpenType](https://www.microsoft.com/typography/otspec/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



