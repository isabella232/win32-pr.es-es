---
description: El ejemplo descrito en la sección titulada Creación de un &\# condicional 0034; Espera.
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: Agregar texto almacenado en una propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965a90c5e0701c54959bb4eae26b26c07ad7b4cbae8aefa6bdf346542b6a5cf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105455"
---
# <a name="adding-text-stored-in-a-property"></a>Agregar texto almacenado en una propiedad

El ejemplo descrito en la sección titulada [Creación de un condicional "Espere . . . " Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md) muestra un cuadro de diálogo con texto que dice: "Espere mientras se complete el costo del espacio en disco". Esto se puede hacer simplemente colocando un [control](text-control.md) de texto en el cuadro de diálogo y especificando la cadena de texto en la columna Texto de la [tabla Control](control-table.md). En este caso, la información sobre el estilo de fuente debe incrustarse en la cadena. El autor debe establecer la fuente y el estilo de fuente mediante el prefijo de la cadena de caracteres con { \\ *style*}. Donde *style* es un identificador de estilo de fuente enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Este método de agregar texto se ilustra varias veces en [Un ejemplo de instalación](an-installation-example.md).

Un autor de una interfaz de usuario también puede almacenar texto en una propiedad. En el ejemplo siguiente se muestra esto y cómo se puede usar ControlEvents para mostrar cadenas de texto alternativas.

El objetivo de este ejemplo es volver a colocar un cuadro **de diálogo WaitForCosting** mientras se ejecuta una tarea en segundo plano. La diferencia con el nuevo escenario es que si el usuario cancela el cuadro de diálogo **WaitForCosting** y, a continuación, intenta activar el control antes de que la tarea en segundo plano haya finalizado una segunda vez, el cuadro **WaitForCosting** vuelve a aparecer mostrando un mensaje alternativo: "El costo del espacio en disco todavía se está ejecutando. Puede seguir esperando o volver al cuadro de selección principal para salir de esta secuencia".

**Para mostrar un cuadro de diálogo "Please Wait" (Esperar) que muestra mensajes alternativos**

1.  Comience agregando un cuadro de **diálogo Condicional WaitForCosting** a un cuadro de diálogo Selección tal como se describe en Creación de un condicional ["Espere . . " Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).
2.  Coloque un [control de texto](text-control.md) en el cuadro de diálogo **WaitForCosting** mediante la creación de un registro en la [tabla Control](control-table.md). Escriba el identificador del cuadro de **diálogo WaitForCosting** en la columna \_ Diálogo . Escriba el identificador del control Texto en la columna Control . Especifique el tipo de control como Texto en la columna Tipo.
3.  Especifique el [atributo control Position](position-control-attribute.md) para el control de texto especificando las coordenadas horizontal y vertical de la esquina superior izquierda del control en las columnas X e Y de la tabla [Control](control-table.md). Use píxeles como unidades de distancia.
4.  Especifique el ancho y alto del control de texto especificando estas dimensiones en las columnas Width y Height de la [tabla Control](control-table.md). Use píxeles como unidades de longitud.
5.  Las columnas Property y Control Next de la tabla Control no afectan a los controles Text y se pueden \_ dejar en blanco en este caso.
6.  Especifique los atributos de control para el control Texto que están asociados a marcas de bits. Agregue los valores de bits individuales juntos y escriba el total en la columna Atributos de la tabla Control. Estos son los atributos de control [Visible,](visible-control-attribute.md) [Bloqueado,](sunken-control-attribute.md) [Habilitado,](enabled-control-attribute.md) [Transparente,](transparent-control-attribute.md) [NoWrap](nowrap-control-attribute.md)y [NoPrefix.](noprefix-control-attribute.md) La combinación de bits que muestran un control de texto en un fondo opaco, con texto encapsulado es 0, por lo tanto, escriba 0 o deje la columna Atributos en blanco.
7.  La columna Texto de la tabla Control se puede dejar en blanco. El control Texto muestra la cadena de texto que es el valor del atributo [de](text-control-attribute.md) control Text. El método para establecer este atributo se describe en los pasos posteriores de este procedimiento.
8.  Agregue un registro en la [tabla Property para](property-table.md) definir la propiedad de mensaje FirstMessage. Esta propiedad es una cadena que contiene el estilo de fuente y el texto del primer mensaje. Escriba el nombre FirstMessage en la columna Propiedad. En la columna Valor, escriba la cadena: "{ WaitStyle}Espere mientras se complete el costo \\ del espacio en disco". Donde WaitStyle es un identificador de uno de los estilos de fuente enumerados en la columna TextStyle de la [tabla TextStyle](textstyle-table.md).
9.  Agregue un registro en la [tabla Property para](property-table.md) definir la propiedad de mensaje SecondMessage. Esta propiedad es una cadena que contiene el estilo de fuente y el texto del segundo mensaje. Escriba el nombre SecondMessage en la columna Propiedad. En la columna Valor, escriba la cadena : "{ \\ WaitStyle}El costo del espacio en disco todavía se está ejecutando. Puede seguir esperando o volver al cuadro de selección principal para salir de esta secuencia".
10. Agregue un registro en la [tabla Property para](property-table.md) definir la propiedad waitMessage message. Esta propiedad es una cadena que contiene el estilo de fuente y el texto del mensaje que se muestra en el cuadro de diálogo **WaitForCosting** si el usuario intenta activar un botón de inserción antes de que se complete el costo. Escriba el nombre WaitMessage en la columna Propiedad. En la columna Valor de la tabla Property, escriba: FirstMessage.
11. Agregue un [control SetProperty ControlEvent](setproperty-controlevent.md) a la [tabla ControlEvent](controlevent-table.md) que inicialice WaitMessage en FirstMessage cada vez que se abra **un cuadro de diálogo** Nueva selección. Escriba el identificador del cuadro de diálogo que aparece justo antes del cuadro de diálogo Selección de la secuencia del cuadro de diálogo en la columna \_ Diálogo . Escriba el identificador del control en este cuadro de diálogo que se usa para abrir el cuadro de diálogo Selección en la columna \_ Control . Escriba \[ WaitMessage \] en la columna Evento. Escriba \[ FirstMessage \] en la columna Argumento. Escriba 1 en la columna Condición y deje la columna Orden en blanco.
12. Agregue un [control SetProperty ControlEvent](setproperty-controlevent.md) a la [tabla ControlEvent](controlevent-table.md) que establece Waitmessage en SecondMessage si el usuario cierra el cuadro de diálogo **WaitForCosting** antes de que se haya completado el costo del espacio en disco. Escriba el identificador del cuadro de **diálogo WaitForCosting** en la columna \_ Diálogo . Escriba el identificador del control Texto en la columna \_ Control . Escriba \[ WaitMessage \] en la columna Evento. Escriba \[ SecondMessage \] en la columna Argumento. Escriba NOT [**CostingComplete en**](costingcomplete.md) la columna Condición y deje la columna Ordering en blanco.
13. En el paso siguiente se vincula el atributo de control Text al controlEvent que genera el **cuadro de diálogo WaitForCosting.** Esto hace que el instalador pase el valor de la propiedad WaitMessage al atributo de control Text cada vez que el usuario abre un cuadro de diálogo **WaitForCosting.**
14. Suscriba el atributo de control Text del control Text al [control SpawnWaitDialog,](spawnwaitdialog-controlevent.md) que abre el cuadro de diálogo **WaitForCosting** agregando un registro a la [tabla EventMapping](eventmapping-table.md). Escriba el identificador del cuadro **de diálogo WaitForCosting** en la columna \_ Diálogo. Escriba el identificador del control Texto en la columna \_ Control . Escriba SpawnWaitDialog en la columna Evento. Escriba Text, el identificador del atributo de control Text, en la columna Atributo de la tabla EventMapping.

 

 



