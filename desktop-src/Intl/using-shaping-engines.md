---
description: Uniscribe usa varios motores de modelado que contienen el conocimiento de diseño para scripts concretos.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Uso de motores de modelado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb0fd75e0612340bc5051f844dda5e9d66c22eb56a88b0c497891a15faaa75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897855"
---
# <a name="using-shaping-engines"></a>Uso de motores de modelado

Uniscribe usa varios motores de modelado que contienen el conocimiento de diseño para scripts concretos. También aprovecha el motor de modelado de diseño OpenType para controlar características de script específicas de fuente, como la generación de glifos, la medición de extensiones y la compatibilidad con separación de palabras. Uniscribe administra la reordenación de caracteres bidireccionales mediante el algoritmo bidireccional Unicode y entiende los formatos de fuente de diseño que no son OpenType para la forma árabe, hebreo y tailandés.

Dado que los intervalos de puntos de código exactos asignados a cada motor de modelado pueden variar, los números de script no se publican, a excepción de SCRIPT \_ UNDEFINED. Sin embargo, la aplicación puede probar los atributos de los scripts llamando a la [**función ScriptGetProperties,**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) que tiene acceso a la tabla de propiedades de script global. La aplicación puede usar las propiedades de script global para ayudar a combinar sus propias reglas de diseño con las divisiones necesarias del motor de modelado.

La aplicación accede a un motor de modelado con una llamada a la [**función ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Todos los motores de modelado de scripts complejos, los motores de modelado de dígitos y los motores de modelado ASCII validan la fuente indicada en el identificador de contexto del dispositivo antes de dar forma. Los scripts complejos deben dar forma mediante el script devuelto por la [**función ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para que sean legibles. Otras ejecuciones siguen siendo legibles si se han dado forma con SCRIPT UNDEFINED especificado en el miembro eScript de la estructura \_ [**SCRIPT \_ ANALYSIS,**](/windows/win32/api/usp10/ns-usp10-script_analysis) aunque podrían perder calidad tipográfica. 

[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) devuelve 0 si se realiza correctamente, o USP E SCRIPT NOT IN FONT si la fuente proporcionada por la aplicación no contiene \_ \_ \_ \_ glifos suficientes ni tablas \_ de modelado. Si la aplicación especifica SCRIPT UNDEFINED y la fuente no admite algunos \_ caracteres, la función sigue siendo correcta. En este caso, la aplicación debe examinar el búfer de salida del glifo en busca de la presencia de glifos que faltan. Para obtener estrategias para tratar con glifos que faltan, vea [Using Font Fallback](using-font-fallback.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



