---
description: Los programas de lector de pantalla solo pueden leer el texto de un control RadioButtonGroup creado en la columna de texto de la tabla RadioButton.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Agregar texto adicional a los botones de radio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001760"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Agregar texto adicional a los botones de radio

Los programas de lector de pantalla solo pueden leer el texto de un [control RadioButtonGroup](radiobuttongroup-control.md) creado en la columna de texto de la [tabla RadioButton](radiobutton-table.md). Si este texto es una descripción insuficiente de los botones de radio, se pueden agregar [controles de texto](text-control.md) superpuestos para proporcionar texto descriptivo adicional. Estos controles de texto deben superponerse entre sí en el cuadro de diálogo y tienen condiciones establecidas en la [tabla ControlCondition](controlcondition-table.md) para que solo se muestre un control de texto a la vez. Los controles de texto no deben superponerse en el control RadioButtonGroup u otros controles del cuadro de diálogo, ya que esto hace que los controles sean invisibles para los lectores de pantalla. Cuando el usuario mantiene el cursor sobre el control de texto, el programa de lectura de pantalla lee el texto adicional.

En el ejemplo siguiente, el cuadro de diálogo de ejemplo tiene un control RadioButtonGroup denominado colores con dos opciones para el valor de la propiedad el color. Para cada opción hay un control de texto con una condición que se va a ocultar o mostrar, dependiendo de la opción actual seleccionada para el color. Se define el valor de color Initial en la tabla de propiedades. Los controles de texto tienen el texto descriptivo adicional creado en el campo de texto de la tabla RadioButton. Cuando un usuario mantiene el cursor sobre el control de texto en el cuadro de diálogo, el lector de pantalla puede leer la descripción adicional de la opción actual.

[Tabla de cuadro de diálogo](dialog-table.md)



| Diálogo   | HCentering | VCentering | Ancho | Alto | Atributos | Title                    | Controlar \_ primero | \_Valor predeterminado del control | \_Cancelar control |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Botones de radio accesibles | Colores         | Siguientes             |                 |



 

[Tabla de control](control-table.md)



| Diálogo\_ | Control    | Tipo             | X   | Y   | Ancho | Alto | Atributos | Propiedad | Texto                               | Control \_ siguiente | Ayuda |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Colores     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | Color |                                    | Siguientes          |      |
| MySample | HowIsBlue  | Texto             | 20  | 80  | 150   | 15     | 2          |          | Es como el cielo en un día claro. |               |      |
| MySample | HowIsGreen | Texto             | 20  | 80  | 150   | 15     | 2          |          | Es como hierba en el muelle.    |               |      |



 

[Tabla RadioButton](radiobutton-table.md)



| Propiedad | Pedido | Value | X   | Y   | Ancho | Alto | Texto   | Ayuda |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| Color | 1     | Azul  | 10  | 10  | 80    | 15     | &azul  |      |
| Color | 2     | Verde | 10  | 30  | 80    | 15     | &verde |      |



 

[Tabla de propiedades](property-table.md)



| Propiedad | Value |
|----------|-------|
| Color | Azul  |



 

[Tabla ControlCondition](controlcondition-table.md)



| Diálogo\_ | control\_  | Acción | Condición                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | Ocultar   | Color <>  "Blue"  |
| MySample | HowIsBlue  | Mostrar   | Color = "Blue"         |
| MySample | HowIsGreen | Ocultar   | Color <>  "Green" |
| MySample | HowIsGreen | Mostrar   | Color = "verde"        |



 

Para obtener más información, vea [accesibilidad](accessibility.md).

 

 



