---
description: ICE34 valida que cada botón de radio de cada control RadioButtonGroup tiene una propiedad en la columna propiedad de la tabla RadioButton que especifica su grupo de botones de radio.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667755"
---
# <a name="ice34"></a>ICE34

ICE34 valida que cada botón de radio de cada [control RadioButtonGroup](radiobuttongroup-control.md) tiene una propiedad en la columna propiedad de la [tabla RadioButton](radiobutton-table.md) que especifica su grupo de botones de radio. ICE34 valida que esta propiedad existe y está establecida en un valor predeterminado en la [tabla de propiedades](property-table.md) que es igual a uno de los valores de botón de radio del grupo en la columna valor de la tabla RadioButton.

Un grupo de botones de radio debe tener un valor predeterminado para que los usuarios puedan seleccionar una opción mediante la tecla TAB. Esto es necesario para que la accesibilidad de los usuarios sea correcta.

ICE34 informa de las tablas que faltan.

## <a name="result"></a>Resultado

ICE34 expone un mensaje de error si hay un botón de radio que especifica una propiedad no válida.

## <a name="example"></a>Ejemplo

ICE34 notifica los siguientes errores para el ejemplo que se muestra.



| Error ICE34                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El control dialoga. Control2 debe tener una propiedad porque es de tipo RadioButtonGroup.                                                                                      | Hay un [control RadioButtonGroup](radiobuttongroup-control.md), sin el bit de [control indirecto](indirect-control-attribute.md) establecido en la columna Attributes de la [tabla de control](control-table.md), que no tiene una propiedad enumerada en la columna Property. |
| Quizás no es un valor predeterminado válido para RadioButtonGroup con la propiedad Property3. El valor debe aparecer como una opción en la tabla RadioButtonGroup.                 | Existe un valor predeterminado para una propiedad especificada en la columna valor de la [tabla de propiedades](property-table.md) que no es uno de los valores del grupo de botones de radio especificado en la columna valor de la [tabla RadioButton](radiobutton-table.md).                  |
| Se debe definir la propiedad PropertyB porque es una propiedad indirecta de un cuadro de diálogo de control RadioButtonGroup. Control4                                                       | La propiedad a la que hace referencia este grupo RadioButton es una propiedad indirecta y el valor de la propiedad indirecta no es una de las opciones del grupo RadioButton.                                                                                                       |
| Quizás no es un valor predeterminado válido para la propiedad propertya. La propiedad es una propiedad RadioButtonGroup indirecta de control dialoga. Control5 (a través de la propiedad Property5). | El valor de la propiedad indirecta a la que se hace referencia a través del control no es ninguno de los valores predeterminados para ese RadioButtonGroup.                                                                                                                                                    |



 

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Tipo             | Atributos | Propiedad  |
|---------|----------|------------------|------------|-----------|
| Cuadro de diálogo | Control1 | RadioButtonGroup | 0          | Property1 |
| Cuadro de diálogo | Control2 | RadioButtonGroup | 0          |           |
| Cuadro de diálogo | Control3 | RadioButtonGroup | 0          | Property3 |
| Cuadro de diálogo | Control4 | RadioButtonGroup | 8          | Property4 |
| Cuadro de diálogo | Control5 | RadioButtonGroup | 8          | Property5 |



 

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad  | Value     |
|-----------|-----------|
| Property1 | Sí       |
| Property3 | Es posible     |
| Property4 | PropertyB |
| Property5 | Propiedad a |
| Propiedad a | Es posible     |



 

[Tabla RadioButton](radiobutton-table.md) (parcial)



| Propiedad  | Pedido | Value |
|-----------|-------|-------|
| Property1 | 1     | Sí   |
| Property1 | 2     | Ahora   |
| Property2 | 1     | Sí   |
| Property2 | 2     | No    |
| Property3 | 1     | Sí   |
| Property3 | 2     | No    |
| Property4 | 1     | Sí   |
| Property4 | 2     | No    |
| Propiedad a | 1     | Sí   |
| Propiedad a | 2     | No    |
| PropertyB | 1     | Sí   |
| PropertyB | 2     | No    |



 

Para corregir los errores que se indican en esta ICE, compruebe lo siguiente:

-   Cada entrada de control RadioButton sin el conjunto de atributos indirectos tiene una propiedad que aparece en la columna propiedad:
-   Que cada propiedad de este tipo tiene al menos una entrada correspondiente en la tabla RadioButton.
-   Cada una de estas propiedades se define en la tabla de propiedades, con un valor que es una de las opciones de la tabla RadioButton.
-   Todas las propiedades a las que se hace referencia en la columna de propiedades de un control RadioButton con el conjunto de atributos indirecto se definen en la tabla de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



