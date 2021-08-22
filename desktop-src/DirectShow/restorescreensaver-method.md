---
description: El método DVDAdm.RestoreScreenSaver restaura la configuración del protector de pantalla del sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 684250b237105e391472237a5e7093855dd82ef5b59ffbbaa20ebecf386da302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696975"
---
# <a name="restorescreensaver-method"></a>Método RestoreScreenSaver

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `DVDAdm.RestoreScreenSaver` método restaura la configuración del protector de pantalla del sistema.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Por lo general, una aplicación de DVD deshabilitará el protector de pantalla del sistema al iniciar estableciendo la propiedad [**DisableScreenSaver**](disablescreensaver-property.md) en true y, a continuación, volverá a habilitar el protector de pantalla cuando se cierre la aplicación de DVD mediante una llamada a `RestoreScreenSaver` . Si una aplicación no usa la configuración del protector de pantalla del sistema, no tiene que llamar a este método ni establecer la **propiedad DisableScreenSaver.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



