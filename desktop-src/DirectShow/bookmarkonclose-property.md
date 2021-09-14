---
description: La propiedad DVDAdm.BookmarkOnClose establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario cierre la aplicación.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Propiedad BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161681"
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

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de true.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



