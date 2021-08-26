---
description: La propiedad DVDAdm.BookmarkOnClose establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario cierre la aplicación.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propiedad BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83ed0ef05e2efe7edb3b6494e8f9709b23259207af257957551077dfbbddaba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103345"
---
# <a name="bookmarkonclose-property"></a>Propiedad BookmarkOnClose

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario cierre `DVDAdm.BookmarkOnClose` la aplicación.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano, que si es true, indica que el control MSDVDAdm guardará un marcador de toda la configuración de DVD, incluida la posición en el disco, el nivel parental y el país o región parental cuando el usuario cierre la aplicación del reproductor de DVD.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura con un valor predeterminado de true.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



