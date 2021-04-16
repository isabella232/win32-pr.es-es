---
description: La propiedad DVDAdm. DefaultSubpictureLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de subimagen.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propiedad DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538241"
---
# <a name="defaultsubpicturelcid-property"></a>Propiedad DefaultSubpictureLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm.DefaultSubpictureLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de subimagen.

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el LCID de la subimagen predeterminada especificada por el usuario, tal y como se almacena en la configuración del registro de la aplicación de DVD. Este valor no es necesariamente el mismo que el flujo de la subimagen predeterminada que se creó en el DVD. Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de la plataforma.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Si no se especifica ningún LCID de subimagen predeterminado, el objeto MSDVDAdm reproducirá el flujo de subimagen que está marcado como la secuencia predeterminada en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



