---
description: Ver información de la topología
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Ver información de la topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696861"
---
# <a name="viewing-topology-information"></a>Ver información de la topología

En TopoEdit, cada elemento de topología, como nodos, entradas de nodo y salidas de nodo, tiene un almacén de atributos asociado que administra el comportamiento del nodo. Para ver los atributos, seleccione el elemento y el **Panel atributos** muestra la información. En el caso de las topologías que se cargan desde un archivo XML, es posible que algunos de los nodos no muestren el almacén de atributos completo. Para ver el almacén de atributos completo, resuelva la topología. Para obtener más información, vea [resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md).

En la tabla siguiente se muestra el elemento de topología y los atributos que muestra el panel.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento de topología</th>
<th>Atributos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nodos de topología</td>
<td><ul>
<li><a href="topology-node-attributes.md">Atributos de nodo de topología</a> para todos los nodos.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Atributos de descriptor de presentación</a> solo para nodos de origen.<br/></li>
<li>Información de autoridad de confianza de entrada y salida para los nodos de transformación y de salida.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Entrada de nodo</td>
<td><ul>
<li><a href="media-type-attributes.md">Atributos de tipo de medio</a> para todos los nodos.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Salida de nodo</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Atributos de descriptor de flujo</a> solo para nodos de origen.<br/></li>
<li><a href="media-type-attributes.md">Atributos de tipo de medio</a> para todos los nodos.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los valores de atributo, excepto las referencias de puntero y los valores de matriz, se pueden cambiar. Para cambiar un valor de atributo, escriba el nuevo valor junto al atributo y haga clic en **Guardar** en el **Panel atributos**. El nuevo valor se actualiza en el almacén de atributos y se aplica a la topología solo después de resolverlo.

## <a name="to-add-a-new-attribute-for-a-node"></a>Para agregar un nuevo atributo para un nodo

1.  Seleccione el nodo haciendo clic en él en el **Panel topología**.

    Los atributos que se establecen en el nodo se muestran en el **Panel atributos**.

2.  En el **Panel atributos**, haga clic en **Agregar**.

    Se abrirá el cuadro de diálogo **Agregar atributo** .

3.  En la primera lista desplegable, elija la categoría de atributo.

    Las categorías dependen del nodo de la topología. Por ejemplo, para el nodo de origen, la lista desplegable muestra los **atributos de descriptor de presentación** y los atributos de **nodo** como categorías disponibles.

4.  En la segunda lista desplegable, elija el atributo que desea establecer en el nodo.

5.  En el cuadro de edición, agregue el valor para el atributo.

6.  Haga clic en **Agregar** para agregar el atributo y volver a la ventana principal, o haga clic en **Cancelar** para cancelar la operación.

7.  En el menú **topología** , haga clic en **resolver topología** para establecer el nuevo atributo en la topología.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




