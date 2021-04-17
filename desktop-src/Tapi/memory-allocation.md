---
description: Las aplicaciones deben asignar memoria para estos datos; TAPI y el proveedor de servicios proporcionan los datos. Si la operación es asincrónica, los datos no estarán disponibles hasta que el mensaje de respuesta asincrónica indique que el resultado es correcto.
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: Asignación de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686479"
---
# <a name="memory-allocation"></a>Asignación de memoria

Las aplicaciones deben asignar memoria para estos datos; TAPI y el proveedor de servicios proporcionan los datos. Si la operación es asincrónica, los datos no estarán disponibles hasta que el mensaje de respuesta asincrónica indique que el resultado es correcto.

Todas las estructuras de datos utilizadas para pasar datos entre la aplicación y el TAPI están *acopladas*. Es decir, las estructuras de datos no contienen punteros a subestructuras que contienen componentes de datos de tamaño variable. En su lugar, las estructuras de datos utilizadas para pasar cantidades variables de datos de vuelta a la aplicación deben tener la Metaestructura siguiente:

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

El miembro **dwTotalSize** es el tamaño, en bytes, que se asigna a esta estructura de datos. Marca el final de la estructura de datos y lo establece la aplicación antes de invocar la función que usa esta estructura de datos. La función no lee ni escribe más allá de este tamaño. Una aplicación debe establecer el miembro **dwTotalSize** para indicar el número total de bytes asignados para que TAPI devuelva el contenido de la estructura.

TAPI rellena el miembro **dwNeededSize** . Indica el número de bytes necesarios para devolver todos los datos solicitados. La existencia de campos de tamaño de variable a menudo hace que la aplicación pueda calcular el tamaño de la estructura de datos necesario para asignar. Este campo devuelve el número de bytes realmente necesarios para los datos. Este número puede ser menor que, igual o mayor que **dwTotalSize**, e incluye espacio para el propio miembro de **dwTotalSize** . Si es mayor, la estructura devuelta solo se rellena parcialmente. Si los campos que requiere la aplicación están disponibles en la estructura parcial, no se debe hacer nada más. De lo contrario, la aplicación debe asignar al menos el tamaño de **dwNeededSize** y volver a invocar la función. Normalmente, hay suficiente espacio disponible esta vez para devolver toda la información, aunque es posible que el tamaño pueda haber aumentado de nuevo.

TAPI rellena el miembro **dwUsedSize** si devuelve datos a la aplicación para indicar el tamaño real, en bytes, de la parte de la estructura de datos que contiene datos útiles. Si, por ejemplo, una estructura que se asignó era demasiado pequeña y el campo truncado es un campo de tamaño de variable, **dwNeededSize** es mayor que **dwTotalSize** y el campo truncado se deja vacío. Por lo tanto, el miembro **dwUsedSize** podría ser menor que **dwTotalSize**. No se devuelven los valores de campo parciales.

El siguiente encabezado es la parte fija de la estructura de datos. Contiene los campos normales y los pares de tamaño y desplazamiento que describen los campos de tamaño de variable reales. El campo desplazamiento contiene el desplazamiento en bytes del campo tamaño de variable desde el principio del registro. El campo tamaño contiene el tamaño en bytes del campo tamaño de variable. Si un campo de tamaño de variable está vacío, el campo de tamaño es cero y el desplazamiento se establece en cero. Los campos de tamaño de variable que se truncarían si el tamaño total de la estructura no es suficiente se dejan vacíos. Es decir, su campo size se establece en cero y el desplazamiento se establece en cero. Los campos de tamaño de variable siguen los campos fijos.

Si el proveedor de servicios debe rellenar un miembro de variable, TAPI inicializa el tamaño y los miembros de desplazamiento correspondientes en cero. Si el proveedor de servicios rellena el miembro de variable, debe establecer el tamaño y los miembros de desplazamiento correspondientes en los valores adecuados, incluidos **dwUsedSize** y **dwNeededSize** si establece miembros de variable. El proveedor de servicios no debe truncar un miembro de variable para que quepa en el espacio disponible.

El proveedor de servicios debe iniciar los miembros de variable inmediatamente después de los miembros fijos de la estructura y dejar cualquier espacio adicional al final de la memoria asignada para que TAPI pueda usarlo para los miembros de longitud variable. Puede colocar los miembros de variable en cualquier orden, pero los miembros deben ser contiguos.

 

 



