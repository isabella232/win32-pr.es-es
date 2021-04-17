---
description: La lista espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Acerca de la lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666433"
---
# <a name="about-the-disk-space-list"></a>Acerca de la lista de Disk-Space

La lista espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación. Después de crear una lista de espacio en disco y de agregarle operaciones de archivo, puede consultar la lista para determinar las unidades de destino especificadas por las operaciones de archivo y el espacio en disco necesario en cada unidad.

Al comparar el espacio necesario para el espacio disponible en los discos de destino, puede determinar mediante programación si hay suficiente espacio disponible para la instalación actual.

Puede Agregar o quitar operaciones de archivo en la lista de espacio en disco y recalcular el espacio en disco necesario. Esta funcionalidad permite, por ejemplo, escribir un programa que interactúe con el usuario, permitiéndole elegir qué componentes desean instalar en función del espacio en disco necesario.

Las funciones de lista de espacio en disco comprueban automáticamente si hay copias preexistentes de archivos en el disco de destino. Si se encuentra una versión anterior del archivo, las funciones de lista de espacio en disco calculan el espacio adicional necesario para completar las operaciones de archivo.

Por ejemplo, si una operación de copia especifica que se copie un archivo de 6000 bytes en la unidad C y ya existe una versión de 2000 bytes de ese archivo en la unidad C, las funciones de espacio en disco devolverán un espacio necesario de 4000 bytes. El espacio adicional se usa para reemplazar la versión anterior del archivo por la versión más reciente.

Las funciones de lista de espacio en disco redondean los tamaños de archivo a los límites del clúster de disco.

 

 



