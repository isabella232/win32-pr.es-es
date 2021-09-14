---
description: ICE34 valida que cada botón de radio de cada control RadioButtonGroup tiene una propiedad en la columna Propiedad de la tabla RadioButton que especifica su grupo de botones de radio.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074623"
---
# <a name="ice34"></a>ICE34

ICE34 valida que cada botón de radio de cada [control RadioButtonGroup](radiobuttongroup-control.md) tiene una propiedad en la columna Propiedad de la [tabla RadioButton](radiobutton-table.md) que especifica su grupo de botones de radio. ICE34 valida que esta propiedad existe y se establece en un valor predeterminado en la tabla [Property](property-table.md) que es igual a uno de los valores de botón de radio del grupo en la columna Valor de la tabla RadioButton.

Un grupo de botones de radio debe tener un valor predeterminado para que los usuarios puedan seleccionar una opción con la tecla TAB. Esto es necesario para la accesibilidad adecuada del usuario.

ICE34 notifica que faltan tablas.

## <a name="result"></a>Resultado

ICE34 publica un mensaje de error si hay un botón de radio que especifica una propiedad no válida.

## <a name="example"></a>Ejemplo

ICE34 notifica los siguientes errores para el ejemplo mostrado.



| Error ICE34                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El control DialogA.Control2 debe tener una propiedad porque es de tipo RadioButtonGroup.                                                                                      | Hay un [control RadioButtonGroup](radiobuttongroup-control.md), sin el bit de [control](indirect-control-attribute.md) indirecto establecido en la columna Atributos de la [tabla Control](control-table.md), que no tiene una propiedad enumerada en la columna Propiedad . |
| Quizás no es un valor predeterminado válido para RadioButtonGroup mediante la propiedad Property3. El valor debe aparecer como una opción en la tabla RadioButtonGroup.                 | Hay un valor predeterminado para una propiedad especificada en la columna Valor de la tabla [Property](property-table.md) que no es uno de los valores del grupo de botones de radio especificado en la columna Valor de la [tabla RadioButton](radiobutton-table.md).                  |
| La propiedad PropertyB debe definirse porque es una propiedad indirecta de un control RadioButtonGroup DialogA.Control4                                                       | La propiedad a la que hace referencia este grupo RadioButton es una propiedad indirecta y el valor de la propiedad indirecta no es una de las opciones para el grupo RadioButton.                                                                                                       |
| Quizás no es un valor predeterminado válido para la propiedad PropertyA. La propiedad es una propiedad RadioButtonGroup indirecta del control DialogA.Control5 (a través de la propiedad Property5). | El valor de la propiedad indirecta a la que se hace referencia a través del control no es uno de los valores predeterminados para ese RadioButtonGroup.                                                                                                                                                    |



 

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Tipo             | Atributos | Propiedad.  |
|---------|----------|------------------|------------|-----------|
| DialogA | Control1 | RadioButtonGroup | 0          | Property1 |
| DialogA | Control2 | RadioButtonGroup | 0          |           |
| DialogA | Control3 | RadioButtonGroup | 0          | Propiedad3 |
| DialogA | Control4 | RadioButtonGroup | 8          | Propiedad 4 |
| DialogA | Control5 | RadioButtonGroup | 8          | Propiedad5 |



 

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad.  | Value     |
|-----------|-----------|
| Property1 | Sí       |
| Propiedad3 | Es posible     |
| Propiedad 4 | PropertyB |
| Propiedad5 | PropiedadA |
| PropiedadA | Es posible     |



 

[Tabla RadioButton](radiobutton-table.md) (parcial)



| Propiedad.  | Pedido | Value |
|-----------|-------|-------|
| Property1 | 1     | Sí   |
| Property1 | 2     | Ahora   |
| Property2 | 1     | Sí   |
| Property2 | 2     | No    |
| Propiedad3 | 1     | Sí   |
| Propiedad3 | 2     | No    |
| Propiedad 4 | 1     | Sí   |
| Propiedad 4 | 2     | No    |
| PropiedadA | 1     | Sí   |
| PropiedadA | 2     | No    |
| PropertyB | 1     | Sí   |
| PropertyB | 2     | No    |



 

Para corregir los errores notificados por este ICE, compruebe lo siguiente:

-   Que cada entrada de control RadioButton sin el conjunto de atributos indirectos tiene una propiedad enumerada en la columna Propiedad:
-   Que cada propiedad de este tipo tenga al menos una entrada correspondiente en la tabla RadioButton.
-   Que cada propiedad de este tipo se define en la tabla Property, con un valor que es una de las opciones de la tabla RadioButton.
-   Que todas las propiedades a las que se hace referencia en la columna Property de un control RadioButton con el conjunto de atributos indirectos se definen en la tabla Property.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



