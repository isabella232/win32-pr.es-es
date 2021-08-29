---
description: La lista de espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Acerca de la Disk-Space datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6595d3087ac8ac7913d4ce79acdc7607355eaa232342c5a7e2ef597e4fa5f013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887931"
---
# <a name="about-the-disk-space-list"></a>Acerca de la Disk-Space datos

La lista de espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación. Después de crear una lista de espacio en disco y agregarle operaciones de archivo, puede consultar la lista para determinar las unidades de destino especificadas por las operaciones de archivo y el espacio en disco necesario en cada unidad.

Al comparar el espacio necesario con el espacio disponible en los discos de destino, puede determinar mediante programación si hay espacio suficiente disponible para la instalación actual.

Puede agregar o quitar operaciones de archivo a la lista de espacio en disco y volver a calcular el espacio en disco necesario. Esta funcionalidad le permite, por ejemplo, escribir un programa que interactúe con el usuario, lo que le permite elegir qué componentes quiere instalar en función del espacio en disco necesario.

Las funciones de lista de espacio en disco comprueban automáticamente si hay copias preexistente de archivos en el disco de destino. Si se encuentra una versión anterior del archivo, las funciones de lista de espacio en disco calculan el espacio adicional necesario para completar las operaciones de archivo.

Por ejemplo, si una operación de copia especifica que se copie un archivo de 6000 bytes en la unidad C y que ya exista una versión de 2000 bytes de ese archivo en la unidad C, las funciones de espacio en disco devolverían un espacio necesario de 4000 bytes. El espacio adicional se usa para reemplazar la versión anterior del archivo por la versión más reciente.

La lista de espacio en disco funciona redondean los tamaños de archivo a los límites del clúster de disco.

 

 



