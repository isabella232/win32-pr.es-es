---
description: Ver información de topología
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Ver información de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf29f28ac419da7df14d90efb50919634d7409b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248529"
---
# <a name="viewing-topology-information"></a>Ver información de topología

En TopoEdit, cada elemento de topología, como nodos, entradas de nodo y salidas de nodo, tiene un almacén de atributos asociado que administra el comportamiento del nodo. Para ver los atributos, seleccione el elemento y el **panel Atributos** mostrará la información. En el caso de las topologías que se cargan desde un archivo XML, es posible que algunos de los nodos no muestren todo el almacén de atributos. Para ver todo el almacén de atributos, resuelva la topología. Para obtener más información, [vea Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md).

En la tabla siguiente se muestra el elemento de topología y los atributos que muestra el panel.




| Elemento de topología | Atributos | 
|---------------|------------|
| Nodos de topología | <ul><li><a href="topology-node-attributes.md">Atributos de nodo de topología</a> para todos los nodos.<br /></li><li><a href="presentation-descriptor-attributes.md">Atributos del descriptor de presentación</a> solo para nodos de origen.<br /></li><li>Información de autoridad de confianza de entrada y salida para nodos de transformación y salida.<br /></li></ul> | 
| Entrada de nodo | <ul><li><a href="media-type-attributes.md">Atributos de tipo multimedia</a> para todos los nodos.</li></ul> | 
| Salida del nodo | <ul><li><a href="stream-descriptor-attributes.md">Atributos de descriptor de flujo</a> solo para nodos de origen.<br /></li><li><a href="media-type-attributes.md">Atributos de tipo multimedia</a> para todos los nodos.<br /></li></ul> | 




 

Los valores de atributo, excepto las referencias de puntero y los valores de matriz, se pueden cambiar. Para cambiar un valor de atributo, escriba el nuevo valor junto al atributo y haga clic **en Guardar en** el panel **Atributos**. El nuevo valor se actualiza en el almacén de atributos y se aplica a la topología solo después de resolverlo.

## <a name="to-add-a-new-attribute-for-a-node"></a>Para agregar un nuevo atributo para un nodo

1.  Seleccione el nodo haciendo clic en él en el **panel Topología**.

    Los atributos que se establecen en el nodo se muestran en el **panel Atributos**.

2.  En el panel **Atributos ,** haga clic **en Agregar.**

    Se abrirá el **cuadro de diálogo Agregar** atributo .

3.  En la primera lista desplegable, elija la categoría Atributo.

    Las categorías dependen del nodo de topología. Por ejemplo, para el nodo de origen, la lista desplegable muestra Atributos **del descriptor** de presentación y Atributos **de nodo** como categorías disponibles.

4.  En la segunda lista desplegable, elija el atributo que desea establecer en el nodo.

5.  En el cuadro de edición, agregue el valor del atributo .

6.  Haga **clic en** Agregar para agregar el atributo y volver a la ventana principal, o haga clic en **Cancelar** para cancelar la operación.

7.  En el **menú Topología,** haga clic **en Resolver topología** para establecer el nuevo atributo en la topología.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




