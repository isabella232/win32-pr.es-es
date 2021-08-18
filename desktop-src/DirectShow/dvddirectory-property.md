---
description: La propiedad DVDDirectory establece o recupera el directorio actual del volumen de DVD actual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propiedad DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749105"
---
# <a name="dvddirectory-property"></a>Propiedad DVDDirectory

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDDirectory` propiedad establece o recupera el directorio actual del volumen de DVD actual.

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de cadena que indica la ruta de acceso al directorio raíz del DVD.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Use este método para establecer la ruta de acceso raíz cuando haya más de una unidad de DVD en un sistema. Cuando solo hay una unidad en el sistema y su letra de unidad es superior a "C", el objeto MSWebDVD la encuentra automáticamente. Para un disco DVD-Video estándar, la ruta de acceso raíz debe incluir el directorio de \_ vídeo ts:


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Algunos volúmenes de DVD pueden tener su vídeo en un directorio denominado algo distinto de \_ "video ts". La idea general es que un "volumen de DVD" adicional (el conjunto de . Ifo. VOB y . Los archivos BUP que normalmente se almacenarían en el directorio VIDEO TS) se pueden colocar en un \_ subdirectorio del disco. Al cambiar la raíz para que apunte a este directorio, MSWebDVD funcionará en este volumen de DVD independiente. Habrá disponible un nuevo conjunto de menús, títulos, entre otros, independientemente de los títulos de la raíz de VIDEO TS, a los que ya no se podrá \_ acceder. Estos directorios se denominan "directorios ocultos". En el ejemplo siguiente se muestra cómo establecer un directorio oculto como raíz, donde "hidden" es un marcador de posición para el nombre que los autores del disco han dado al directorio.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



