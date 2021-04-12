---
description: La propiedad DVDAdm. BookmarkOnStop establece o recupera un valor que indica al objeto MSWebDVD si se debe guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario hace clic en el botón detener.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Propiedad BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152514"
---
# <a name="bookmarkonstop-property"></a>Propiedad BookmarkOnStop

La `DVDAdm.BookmarkOnStop` propiedad establece o recupera un valor que indica al objeto MSWebDVD si desea guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario hace clic en el botón **detener** .

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si el objeto MSDVDAdm guardará un marcador de toda la configuración de DVD, incluida la posición en el disco, el nivel parental y el país o región parental.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y su valor predeterminado es false.

Los marcadores solo son válidos para un equipo determinado. Un usuario no puede guardar un marcador y, a continuación, enviarlo a otra persona para que lo lea en otro equipo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



