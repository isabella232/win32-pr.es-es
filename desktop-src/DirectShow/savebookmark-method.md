---
description: El método SaveBookmark guarda la posición y el estado actuales del disco del objeto MSWebDVD para que el usuario pueda volver al mismo lugar más adelante.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Método SaveBookmark (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fec3a109b97c0ccbcb9a98736a01bba625537f1369fa7986cb6b5a669d35b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072719"
---
# <a name="savebookmark-method"></a>SaveBookmark (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método guarda la posición actual del disco y el estado del objeto `SaveBookmark` **MSWebDVD** para que el usuario pueda volver al mismo lugar más adelante.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un marcador es una instantánea del estado actual del navegador de DVD. Esto incluye información como dónde se reproduce en el disco y qué secuencias de audio y subpictures se seleccionan. Al guardar un marcador, el usuario puede cerrar la aplicación, apagar el equipo y volver más tarde para seguir viendo el disco justo donde lo dejó, con toda la configuración igual que antes. Solo se puede guardar un marcador en un momento dado. Cuando se llama `SaveBookmark` a , se sobrescribe el marcador antiguo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RestoreBookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




