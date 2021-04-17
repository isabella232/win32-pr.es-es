---
description: Uniscribe utiliza varios motores de forma que contienen el conocimiento de diseño para scripts determinados.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Usar motores de modelado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653087"
---
# <a name="using-shaping-engines"></a>Usar motores de modelado

Uniscribe utiliza varios motores de forma que contienen el conocimiento de diseño para scripts determinados. También aprovecha el motor de forma de diseño OpenType para administrar características de script específicas de la fuente, como la generación de glifos, la medición de extensiones y la compatibilidad con separación de palabras. Uniscribe administra la reordenación de caracteres bidireccionales mediante el algoritmo bidireccional Unicode, y entiende los formatos de fuente de diseño no OpenType para el modelado árabe, hebreo y tailandés.

Dado que los intervalos de puntos de código exactos asignados a cada motor de forma pueden variar, los números de script no se publican, con la excepción del SCRIPT sin \_ definir. Sin embargo, la aplicación puede probar los atributos de los scripts mediante una llamada a la función [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , que tiene acceso a la tabla de propiedades de script global. La aplicación puede utilizar las propiedades del script global para ayudar a combinar sus propias reglas de diseño con las divisiones del motor de forma necesarias.

La aplicación tiene acceso a un motor de modelado con una llamada a la función [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Todos los motores complejos de modelado de scripts, los motores de modelado de dígitos y los motores de forma ASCII validan la fuente indicada en el identificador de contexto del dispositivo antes de la forma. Se debe dar forma a los scripts complejos mediante el script devuelto por la función [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para que sean legibles. Otras ejecuciones siguen siendo legibles si se forma con SCRIPT sin \_ definir especificado en el miembro **eScript** de la estructura de [**\_ análisis de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) , aunque podrían perder calidad tipográfica.

[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) devuelve 0 si se realiza correctamente o \_ \_ el script \_ de USP E no está \_ en \_ la fuente si la fuente proporcionada por la aplicación no contiene suficientes glifos o tablas de formas. Si la aplicación especifica un SCRIPT sin \_ definir y algunos caracteres no son compatibles con la fuente, la función sigue siendo correcta. En este caso, la aplicación debe examinar el búfer de salida del glifo para detectar la presencia de glifos que faltan. Para conocer las estrategias para tratar los glifos que faltan, vea [usar la reserva de fuentes](using-font-fallback.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



