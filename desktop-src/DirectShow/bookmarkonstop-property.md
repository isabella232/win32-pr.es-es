---
description: La propiedad DVDAdm.BookmarkOnStop establece o recupera un valor que indica al objeto MSWebDVD si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario hace clic en el botón Detener.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: BookmarkOnStop (propiedad)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161680"
---
# <a name="bookmarkonstop-property"></a>BookmarkOnStop (propiedad)

La propiedad establece o recupera un valor que indica al objeto MSWebDVD si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario hace clic en el `DVDAdm.BookmarkOnStop` **botón** Detener.

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si el objeto MSDVDAdm guardará un marcador de todas las configuraciones de DVD, incluida la posición en el disco, el nivel parental y el país o región parental.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura y escritura con un valor predeterminado de false.

Los marcadores solo son válidos para una máquina determinada. Un usuario no puede guardar un marcador y, a continuación, enviarlo a otra persona para leerlo en otro equipo.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



