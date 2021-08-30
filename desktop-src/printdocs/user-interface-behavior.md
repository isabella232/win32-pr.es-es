---
description: Revise una explicación sobre el comportamiento de la interfaz de usuario con respecto a las características y opciones de documentos e impresión.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Interfaz de usuario comportamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e887608dba50092b6b7b94f81052073f2bbfa34c7353b614380e6c0f5ec50bf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947315"
---
# <a name="user-interface-behavior"></a>Interfaz de usuario comportamiento

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Suponga que está creando un cliente printCapabilities que lee en un documento PrintCapabilities y selecciona una o varias opciones de cada característica y las usa para construir un PrintTicket que especifica la configuración que se va a usar para procesar el trabajo. Para cada característica de interés, el cliente debe examinar cada opción y decidir si esa opción es adecuada para la tarea en la mano. Para una opción que no está parametrizada, se puede evaluar accediendo al valor de cada ScoredProperty. En el caso de una opción de tamaño de medio no parametrizado, el cliente determina si las dimensiones de ancho y alto de los medios notificados en cada opción coinciden con las dimensiones necesarias.

En el caso de la opción parametrizada, el cliente debe tener acceso a la instancia ParameterDef que se indica en la instancia ParameterRef contenida en una de las instancias de ScoredProperty. ParameterDef define normalmente el intervalo de valores permitido para el parámetro, así como las unidades (pulgadas, mm, y así sucesivamente) representadas por el valor. Si las dimensiones necesarias se encuentran dentro del intervalo de valores permitido para cada uno de los parámetros, el cliente tiene la tarea adicional de inicializar los parámetros (mediante una instancia parameterInit) en PrintTicket. Se trata de una tarea especialmente importante. Por ejemplo, un PrintTicket no debe especificar un tamaño de medio personalizado sin especificar las dimensiones de los medios, ya que el PrintTicket resultante será ambiguo e indefinido.

Se debe controlar un conjunto de circunstancias similar si el cliente es una interfaz de usuario. La interfaz de usuario normalmente muestra los valores de las instancias scoredProperty definidas para cada opción. Para mayor claridad, es esencial mostrar el intervalo y las unidades permitidos para los parámetros en una opción con parámetros. Además, si el usuario selecciona la opción parametrizada, la interfaz de usuario (UI) debe pedir al usuario que escriba el valor que se usará para inicializar cada parámetro. Por último, la interfaz de usuario debe crear un PrintTicket que refleje todas las selecciones del usuario.

Para obtener más información sobre la construcción de PrintTicket y la especificación de la inicialización de parámetros, vea [Creating a Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Para obtener información sobre cómo desreferenciar instancias de ParameterRef e interpretar instancias de ParameterDef, vea [Usar parámetros](using-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



