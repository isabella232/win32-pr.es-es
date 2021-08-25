---
description: La propiedad DVDAdm.DefaultMenuLCID establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para los menús.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propiedad DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 939f65ad41cb184f38e2a30392030ca67066fe203f7952441cc2f77b1db95242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906896"
---
# <a name="defaultmenulcid-property"></a>Propiedad DefaultMenuLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario `DVDAdm.DefaultMenuLCID` para los menús.

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor Entero que representa el LCID tal y como se almacena en la configuración del Registro para la aplicación de DVD. Este valor no es necesariamente el mismo que el idioma de menú predeterminado que se ha escrito en el DVD. Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de plataforma.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Si no se especifica ningún LCID de menú predeterminado, el objeto MSDVDAdm usará el idioma marcado como idioma de menú predeterminado en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



