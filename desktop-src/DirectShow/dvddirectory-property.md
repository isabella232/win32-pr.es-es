---
description: La propiedad DVDDirectory establece o recupera el directorio actual del volumen de DVD actual.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propiedad DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906630"
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

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Use este método para establecer la ruta de acceso raíz cuando hay más de una unidad de DVD en un sistema. Cuando solo hay una unidad en el sistema y su letra de unidad es superior a "C", el objeto MSWebDVD lo encuentra automáticamente. En el caso de un disco de DVD-Video estándar, la ruta de acceso raíz debe incluir el directorio de vídeo de TS \_ :


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



Algunos volúmenes de DVD pueden tener su vídeo en un directorio cuyo nombre no sea "vídeo \_ TS". La idea general es que un "volumen de DVD" adicional (el conjunto de. IFO. VOB, y. Los archivos BUP que normalmente se almacenarían en el \_ Directorio de vídeo TS se pueden colocar en un subdirectorio del disco. Al cambiar la raíz para que apunte a este directorio, MSWebDVD funcionará en este volumen de DVD independiente. Hay disponible un nuevo conjunto de menús, títulos, etc., independientemente de los títulos de la raíz de TS de vídeo \_ , que ya no serán accesibles. Estos directorios se denominan "directorios ocultos". En el ejemplo siguiente se muestra cómo establecer un directorio oculto como raíz, donde "Hidden" es un marcador de posición para el nombre que los autores del disco han asignado al directorio.


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



