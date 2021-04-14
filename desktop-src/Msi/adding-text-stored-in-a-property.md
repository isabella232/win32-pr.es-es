---
description: El ejemplo descrito en la sección titulada creación de un &condicional \# 0034; Espera.
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: Agregar texto almacenado en una propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d43910b946db737d2b306d7c75f6683401eee0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423880"
---
# <a name="adding-text-stored-in-a-property"></a>Agregar texto almacenado en una propiedad

En el ejemplo que se describe en la sección titulada [creación de una instrucción condicional, espere... "Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md) muestra un cuadro de diálogo con texto que dice:" espere mientras se completa el costo del espacio en disco ". Esto puede hacerse simplemente colocando un [control de texto](text-control.md) en el cuadro de diálogo y escribiendo la cadena de texto en la columna de texto de la [tabla de control](control-table.md). En este caso, la información sobre el estilo de fuente debe estar incrustada en la cadena. El autor debe establecer el estilo de fuente y fuente prefijando la cadena de caracteres con { \\ *Style*}. Donde *Style* es un identificador de estilo de fuente que se muestra en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Este método de agregar texto se muestra varias veces en [un ejemplo de instalación](an-installation-example.md).

Un autor de una interfaz de usuario también puede almacenar texto en una propiedad. En el ejemplo siguiente se muestra cómo se puede usar ControlEvents para mostrar cadenas de texto alternativas.

El objetivo de este ejemplo es volver a colocar un cuadro de diálogo de **WaitForCosting** mientras se ejecuta una tarea en segundo plano. La diferencia con el nuevo escenario es que si el usuario cancela el cuadro de diálogo **WaitForCosting** y, a continuación, intenta activar el control antes de que la tarea en segundo plano finalice una segunda vez, el cuadro **WaitForCosting** volverá a aparecer y mostrará un mensaje alternativo: "el costo del espacio en disco sigue en ejecución. Puede continuar esperando o volver al cuadro de selección principal para salir de esta secuencia ".

**Para mostrar un cuadro de diálogo "Espere" que muestre mensajes alternativos**

1.  Comience agregando un cuadro de diálogo **WaitForCosting** condicional a un cuadro de diálogo de selección como se describe en [creación de una condicional "espere... "Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).
2.  Coloque un [control de texto](text-control.md) en el cuadro de diálogo **WaitForCosting** mediante la creación de un registro en la [tabla de control](control-table.md). Escriba el identificador del cuadro de diálogo **WaitForCosting** en la columna del cuadro de diálogo \_ . Escriba el identificador del control de texto en la columna de control. Especifique el tipo de control como texto en la columna tipo.
3.  Especifique el [atributo de control de posición](position-control-attribute.md) para el control de texto escribiendo las coordenadas horizontal y vertical de la esquina superior izquierda del control en las columnas X e y de la [tabla de control](control-table.md). Use píxeles como unidades de distancia.
4.  Especifique el ancho y el alto del control de texto escribiendo estas dimensiones en las columnas ancho y alto de la [tabla de control](control-table.md). Use píxeles como unidades de longitud.
5.  Las columnas propiedad y control \_ siguientes de la tabla de control no afectan a los controles de texto y pueden dejarse en blanco en este caso.
6.  Especifique los atributos de control para el control de texto que están asociados a marcas de bits. Agregue los valores de bit individuales juntos y especifique el total en la columna Attributes de la tabla de control. Estos son los atributos de control [visible](visible-control-attribute.md), [Sunken](sunken-control-attribute.md), [habilitado](enabled-control-attribute.md), [transparente](transparent-control-attribute.md), [noWrap](nowrap-control-attribute.md)y [noprefix](noprefix-control-attribute.md) . La combinación de bits que muestra un control de texto en un fondo opaco, con texto ajustado es 0, por lo tanto, escriba 0 o deje la columna atributos en blanco.
7.  La columna de texto de la tabla de control puede dejarse en blanco. El control de texto muestra la cadena de texto que es el valor del atributo de control de [texto](text-control-attribute.md) . El método para establecer este atributo se describe en los pasos siguientes de este procedimiento.
8.  Agregue un registro en la [tabla de propiedades](property-table.md) para definir la propiedad de mensaje FirstMessage. Esta propiedad es una cadena que contiene el estilo y el texto de la fuente para el primer mensaje. Escriba el nombre FirstMessage en la columna propiedad. En la columna valor, escriba la cadena: "{ \\ WaitStyle} espere a que se complete el costo de espacio en disco". Donde WaitStyle es un identificador de uno de los estilos de fuente que aparecen en la columna TextStyle de la [tabla TextStyle](textstyle-table.md).
9.  Agregue un registro en la [tabla de propiedades](property-table.md) para definir la propiedad de mensaje SecondMessage. Esta propiedad es una cadena que contiene el estilo y el texto de la fuente para el segundo mensaje. Escriba el nombre SecondMessage en la columna propiedad. En la columna valor, escriba la cadena: "{ \\ WaitStyle} el costo del espacio en disco sigue en ejecución. Puede continuar esperando o volver al cuadro de selección principal para salir de esta secuencia ".
10. Agregue un registro en la [tabla de propiedades](property-table.md) para definir la propiedad del mensaje WaitMessage. Esta propiedad es una cadena que contiene el estilo de fuente y el texto para el mensaje que se muestra en el cuadro de diálogo **WaitForCosting** si el usuario intenta activar un botón de reenvío antes de que se complete el costo. Escriba el nombre WaitMessage en la columna propiedad. En la columna valor de la tabla de propiedades, escriba: FirstMessage.
11. Agregue un [SetProperty ControlEvent,](setproperty-controlevent.md) a la [tabla ControlEvent,](controlevent-table.md) que inicializa WaitMessage en FirstMessage cada vez que se abre un cuadro de diálogo de **selección nuevo** . Escriba el identificador del cuadro de diálogo que viene justo antes del cuadro de diálogo de selección en la secuencia del cuadro de diálogo en la columna del cuadro de diálogo \_ . Escriba el identificador del control en este cuadro de diálogo que se usa para abrir el cuadro de diálogo de selección en la columna de control \_ . Escriba \[ WaitMessage \] en la columna Event. Escriba \[ FirstMessage \] en la columna argument. Escriba 1 en la columna condición y deje la columna orden en blanco.
12. Agregue un [SetProperty ControlEvent,](setproperty-controlevent.md) a la [tabla ControlEvent,](controlevent-table.md) que establezca WaitMessage en SecondMessage si el usuario cierra el cuadro de diálogo **WaitForCosting** antes de que se haya completado el costo del espacio en disco. Escriba el identificador del cuadro de diálogo **WaitForCosting** en la columna de diálogo \_ . Escriba el identificador del control de texto en la columna de control \_ . Escriba \[ WaitMessage \] en la columna Event. Escriba \[ SecondMessage \] en la columna argument. Escriba no [**CostingComplete**](costingcomplete.md) en la columna condición y deje la columna orden en blanco.
13. El paso siguiente vincula el atributo de control de texto con el ControlEvent, que genera el cuadro de diálogo **WaitForCosting** . Esto hace que el instalador pase el valor de la propiedad WaitMessage al atributo de control de texto cada vez que el usuario abra un cuadro de diálogo **WaitForCosting** .
14. Suscríbase el atributo de control de texto del control de texto al [ControlEvent, SpawnWaitDialog](spawnwaitdialog-controlevent.md) que abre el cuadro de diálogo **WaitForCosting** mediante la adición de un registro a la [tabla EventMapping](eventmapping-table.md). Escriba el identificador del cuadro de diálogo **WaitForCosting** en la columna del cuadro de diálogo \_ . Escriba el identificador del control de texto en la columna de control \_ . Escriba SpawnWaitDialog en la columna evento. Escriba el texto, el identificador del atributo de control de texto, en la columna atributo de la tabla EventMapping.

 

 



