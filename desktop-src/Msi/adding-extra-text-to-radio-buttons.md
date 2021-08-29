---
description: Los programas de lector de pantalla solo pueden leer el texto de un control RadioButtonGroup que se ha escrito en la columna Texto de la tabla RadioButton.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Agregar texto adicional a los botones de radio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a1274faeffc3bf98702cc6f549e0be02e0d1d1ba003914d295e4fe004aa39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145988"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Agregar texto adicional a los botones de radio

Los programas de lector de pantalla solo pueden leer el texto de un [control RadioButtonGroup](radiobuttongroup-control.md) que se ha escrito en la columna Texto de la [tabla RadioButton](radiobutton-table.md). Si este texto es una descripción insuficiente de los botones de radio, se pueden agregar controles [text](text-control.md) superpuestos para proporcionar texto descriptivo adicional. Estos controles Text deben superponerse entre sí en el cuadro de diálogo y tener condiciones establecidas en la [tabla ControlCondition](controlcondition-table.md) para que solo se muestra un control Text a la vez. Los controles Text no deben superponerse al control RadioButtonGroup u otros controles del cuadro de diálogo, ya que esto hace que los controles no se superpongan a los lectores de pantalla. Cuando el usuario mantiene el cursor sobre el control Texto, el programa lector de pantalla lee el texto adicional.

En el ejemplo siguiente, el cuadro de diálogo MySample tiene un control RadioButtonGroup denominado Colors con dos opciones para el valor de la propiedad TheColor. Para cada elección hay un control Texto con una condición que se ocultará o mostrará, en función de la opción actual seleccionada para TheColor. Se define un valor TheColor inicial en la tabla Property. Los controles Text tienen el texto descriptivo adicional que se ha escrito en el campo Texto de la tabla RadioButton. Cuando un usuario mantiene el cursor sobre el control Texto en el cuadro de diálogo, el lector de pantalla puede leer la descripción adicional de la opción actual.

[Tabla de diálogos](dialog-table.md)



| Diálogo   | HCentering | VCentering | Ancho | Alto | Atributos | Título                    | Control \_ First | Control \_ predeterminado | Cancelar \_ control |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Botones de radio accesibles | Colores         | Siguientes             |                 |



 

[Tabla de control](control-table.md)



| Diálogo\_ | Control    | Tipo             | X   | Y   | Ancho | Alto | Atributos | Propiedad | Texto                               | Control \_ Siguiente | Ayuda |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Colores     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | TheColor |                                    | Siguientes          |      |
| MySample | HowIsBlue  | Texto             | 20  | 80  | 150   | 15     | 2          |          | Es como el cielo en un día despejado. |               |      |
| MySample | HowIsGreen | Texto             | 20  | 80  | 150   | 15     | 2          |          | Es como el pasto en la primavera.    |               |      |



 

[Tabla RadioButton](radiobutton-table.md)



| Propiedad | Pedido | Value | X   | Y   | Ancho | Alto | Texto   | Ayuda |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| TheColor | 1     | Azul  | 10  | 10  | 80    | 15     | &azul  |      |
| TheColor | 2     | Verde | 10  | 30  | 80    | 15     | &verde |      |



 

[Tabla de propiedades](property-table.md)



| Propiedad | Value |
|----------|-------|
| TheColor | Azul  |



 

[Tabla ControlCondition](controlcondition-table.md)



| Diálogo\_ | control\_  | Acción | Condición                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | Ocultar   | TheColor <> "Blue"  |
| MySample | HowIsBlue  | Mostrar   | TheColor = "Blue"         |
| MySample | HowIsGreen | Ocultar   | TheColor <> "Green" |
| MySample | HowIsGreen | Mostrar   | TheColor = "Green"        |



 

Para obtener más información, vea [Accesibilidad.](accessibility.md)

 

 



