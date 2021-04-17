---
description: ICE23 valida el orden de las pestañas de control de cada cuadro de diálogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667759"
---
# <a name="ice23"></a>ICE23

ICE23 valida el orden de las pestañas de control de cada cuadro de diálogo.

ICE23 valida lo siguiente en la [tabla de cuadro de diálogo](dialog-table.md) y la tabla de [control](control-table.md):

-   Cada registro de la tabla de diálogo especifica un control en la \_ primera columna de control que existe en el cuadro de diálogo especificado por la columna de diálogo.
-   Todos los registros de la tabla de control especifican un control en la \_ columna control siguiente que se encuentra en el mismo cuadro de diálogo que el control enumerado en la columna control, o \_ el control siguiente contiene el valor null.
-   Que siguen las siguientes \_ entradas de control de control a control en la tabla de control, crea un bucle único, cerrado, que vuelve al control inicial. No todos los controles deben estar en el bucle, pero el bucle debe atravesar todos los controles que tengan una entrada en la columna de control \_ siguiente.

## <a name="result"></a>Resultado

ICE23 envía un mensaje de error si el orden de tabulación de los controles no forma un bucle cerrado único en el cuadro de diálogo.

## <a name="example"></a>Ejemplo

ICE23 publicaría los siguientes mensajes de error para el ejemplo mostrado.

-   Dialog1 no tiene ningún control en \_ primer lugar.
-   Controlar el \_ primer cuadro de diálogo Dialog2 hace referencia a ControlX de control inexistente.
-   Dialog3 tiene el orden de tabulación de inactividad en el control ControlB.
-   Dialog4 tiene un orden de tabulación incorrecto en el control ControlC
-   Dialog5 tiene un orden de tabulación incorrecto en el control ControlC.
-   Control \_ siguiente del control Dialog6. ControlC vínculos a un control desconocido.

[Tabla de cuadro de diálogo](dialog-table.md) (parcial)



| Diálogo  | Controlar \_ primero |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Control \_ siguiente |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | ControlB | ControlA      |
| Dialog2 | ControlA | ControlB      |
| Dialog2 | ControlB | ControlA      |
| Dialog3 | ControlA | ControlB      |
| Dialog3 | ControlB |               |
| Dialog4 | ControlA | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialog5 | ControlA | ControlB      |
| Dialog5 | ControlB | ControlC      |
| Dialog5 | ControlC | ControlA      |
| Dialog5 | Controled | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | Controled | ControlA      |



 

Para corregir estos errores, tenga en cuenta lo siguiente en las tablas anteriores y realice los cambios indicados.

No todas las filas de la tabla del cuadro de diálogo tienen un control especificado en la \_ primera columna del control. Cambie la \_ primera columna control del registro Dialog1 de la tabla del cuadro de diálogo a un control que exista en Dialog1.

No todas las filas de la tabla de cuadro de diálogo tienen un control especificado en la \_ primera columna de control que existe en el cuadro de diálogo. Cambie la \_ primera columna de control de Dialog2 a un control que exista en Dialog2.

Las siguientes entradas de control \_ de la tabla de control de control a control no crean un bucle cerrado en todos los casos. Cambie la columna de control \_ siguiente para ControlB en Dialog3 a controla.

Las siguientes entradas de control \_ de la tabla de control de control a control no vuelven al control inicial en todos los casos. Cambie la \_ columna de control siguiente para ControlC en Dialog4 para que haga referencia a controla.

Las siguientes entradas de control de \_ la tabla de control de control a control no atraviesan todos los controles del cuadro de diálogo que tengan una entrada en la columna de control \_ siguiente. Cambie la columna de control \_ siguiente para ControlC en Dialog5 a controled.

El control Next no hace \_ referencia a un control válido que esté en el mismo cuadro de diálogo que el control que aparece en la columna de control. Cambie la \_ columna de control siguiente para ControlC en Dialog6 para que haga referencia a controled.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



