---
description: El método SaveBookmark guarda la posición actual del disco y el estado del objeto MSWebDVD para que el usuario pueda volver al mismo lugar más adelante.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679437"
---
# <a name="savebookmark-method"></a>Método SaveBookmark

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SaveBookmark` método guarda la posición del disco actual y el estado del objeto **MSWebDVD** para que el usuario pueda volver al mismo lugar más adelante.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un marcador es una instantánea del estado actual del navegador de DVD. Esto incluye información como el lugar en el que se reproduce en el disco y los flujos de audio y subimágenes seleccionados. Al guardar un marcador, el usuario puede cerrar la aplicación, apagar el equipo y volver más tarde para seguir viendo el disco en el lugar en el que se quedó, con todas las opciones de configuración como antes. Solo se puede guardar un marcador en un momento dado. Cuando se llama a `SaveBookmark` , se sobrescribe el marcador antiguo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




