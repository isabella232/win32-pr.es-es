---
description: ICE23 valida el orden de tabulación de cada cuadro de diálogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074644"
---
# <a name="ice23"></a>ICE23

ICE23 valida el orden de tabulación de cada cuadro de diálogo.

ICE23 valida lo siguiente en las tablas [Dialog y](dialog-table.md) [Control](control-table.md):

-   Que cada registro de la tabla Dialog especifica un control en la columna Control First que existe en el cuadro de diálogo \_ especificado por la columna Dialog .
-   Que todos los registros de la tabla Control especifiquen un control en la columna Control Siguiente que se encuentra en el mismo cuadro de diálogo que el control enumerado en la columna Control o Control Siguiente contiene el valor \_ \_ NULL.
-   Al seguir las entradas de Control Siguiente del control al control de la tabla Control, se crea un único bucle cerrado que vuelve \_ al control inicial. No todos los controles deben estar en el bucle , pero el bucle debe pasar a través de todos los controles que tienen una entrada en la columna Control \_ Siguiente.

## <a name="result"></a>Resultado

ICE23 publica un mensaje de error si el orden de tabulación de los controles no forma un único bucle cerrado en el cuadro de diálogo.

## <a name="example"></a>Ejemplo

ICE23 publicaría los siguientes mensajes de error para el ejemplo mostrado.

-   Dialog1 no tiene Control \_ First.
-   Control \_ First of dialog Dialog2 hace referencia a control ControlX inexistente.
-   Dialog3 tiene un orden de tabulación de punto de conexión en controlB.
-   Dialog4 tiene un orden de tabulación con formato correcto en el control ControlC
-   Dialog5 tiene un orden de tabulación con formato correcto en el control ControlC.
-   Control \_ Siguiente del control Dialog6.ControlC vincula al control desconocido.

[Tabla de diálogos](dialog-table.md) (parcial)



| Diálogo  | Control \_ First |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Tabla de control](control-table.md) (parcial)



| Diálogo  | Control  | Control \_ Siguiente |
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
| Dialog5 | Controlado | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | Controlado | ControlA      |



 

Para corregir estos errores, tenga en cuenta lo siguiente en las tablas anteriores y realice los cambios indicados.

No todas las filas de la tabla Dialog tienen un control especificado en la columna Control \_ First. Cambie la columna Control First del registro Dialog1 de la tabla \_ Dialog por un control que exista en Dialog1.

No todas las filas de la tabla Dialog tienen un control especificado en la columna Control \_ First que existe en el cuadro de diálogo. Cambie la columna \_ Control First del Cuadro de diálogo2 a un control que exista en Dialog2.

Seguir las entradas De control siguiente de la tabla Control desde el control al control no \_ realiza un bucle cerrado en todos los casos. Cambie la columna Control \_ Siguiente de ControlB en Dialog3 a ControlA.

Seguir las entradas De control siguiente de la tabla Control del control al control no lleva de nuevo al \_ control inicial en todos los casos. Cambie la columna Control \_ Siguiente para ControlC en el cuadro de diálogo 4 para hacer referencia a ControlA.

Si sigue las entradas Control Siguiente de la tabla Control desde el control al control , no pasará a través de todos los controles del cuadro de diálogo que tengan una entrada en \_ la columna Control \_ Siguiente. Cambie la columna Control \_ Siguiente de ControlC en dialog5 a ControlD.

Control Siguiente no hace referencia a un control válido que se encuentra en el mismo cuadro de \_ diálogo que el control enumerado en la columna Control . Cambie la columna Control \_ Siguiente para ControlC en el cuadro de diálogo 6 para hacer referencia a ControlD.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



