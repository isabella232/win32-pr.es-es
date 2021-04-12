---
description: La propiedad DVDAdm. DefaultMenuLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para los menús.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propiedad DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152554"
---
# <a name="defaultmenulcid-property"></a>Propiedad DefaultMenuLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm.DefaultMenuLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para los menús.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el LCID tal y como se almacena en la configuración del registro de la aplicación de DVD. Este valor no es necesariamente el mismo que el idioma del menú predeterminado que se creó en el DVD. Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de la plataforma.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Si no se especifica ningún LCID de menú predeterminado, el objeto MSDVDAdm usará el idioma que esté marcado como idioma predeterminado en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



