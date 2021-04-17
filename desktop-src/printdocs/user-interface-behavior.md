---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Comportamiento de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d475472330c8e3ba2ceb06d0cbde9f3a7fb0be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698010"
---
# <a name="user-interface-behavior"></a>Comportamiento de la interfaz de usuario

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Suponga que está creando un cliente de PrintCapabilities que lee en un documento de PrintCapabilities y selecciona una o varias opciones de cada característica y los utiliza para construir un PrintTicket que especifica la configuración que se va a usar para procesar el trabajo. Para cada característica de interés, el cliente debe examinar cada opción y decidir si esa opción es adecuada para la tarea en cuestión. Para una opción que no tiene parámetros, se puede evaluar accediendo al valor de cada ScoredProperty. En el caso de una opción de tamaño de medio no parametrizado, el cliente determina si las dimensiones de ancho y alto de los medios indicados en cada opción coinciden con las dimensiones requeridas.

En el caso de la opción parametrizada, el cliente debe tener acceso a la instancia de ParameterDef que se indica en la instancia de ParameterRef contenida en una de las instancias de ScoredProperty. Normalmente, ParameterDef define el intervalo de valores permitidos para el parámetro, así como las unidades (pulgadas, mm, etc.) representadas por el valor. Si las dimensiones necesarias se encuentran dentro del intervalo de valores permitido para cada uno de los parámetros, el cliente tiene la tarea adicional de inicializar los parámetros (por medio de una instancia de ParameterInit) en el PrintTicket. Esta tarea es especialmente importante. Por ejemplo, un elemento PrintTicket no debe especificar un tamaño de medio personalizado sin especificar las dimensiones de los medios, porque el elemento PrintTicket resultante será ambiguo y se definirá de forma incorrecta.

Se debe controlar un conjunto de circunstancias similar si el cliente es una interfaz de usuario. La interfaz de usuario muestra normalmente los valores de las instancias de ScoredProperty definidas para cada opción. Para mayor claridad, es esencial mostrar el intervalo permitido y las unidades de los parámetros en una opción parametrizada. Además, si el usuario selecciona la opción parametrizada, la interfaz de usuario (UI) debe solicitar al usuario que escriba el valor que se va a usar para inicializar cada parámetro. Por último, la interfaz de usuario debe crear un PrintTicket que refleje todas las selecciones del usuario.

Para obtener información detallada sobre la construcción de PrintTicket y la especificación de la inicialización de parámetros, vea [crear un Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Para obtener información sobre cómo desreferenciar instancias de ParameterRef e interpretar instancias de ParameterDef, vea [usar parámetros](using-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



