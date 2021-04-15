---
description: El método DVDAdm. RestoreScreenSaver restaura la configuración del protector de pantalla del sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677098"
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

## <a name="remarks"></a>Observaciones

Por lo general, una aplicación de DVD deshabilitará el protector de pantalla del sistema al iniciarse si se establece la propiedad [**DisableScreenSaver**](disablescreensaver-property.md) en true y, a continuación, se vuelve a habilitar el protector de pantalla cuando se cierra la aplicación de DVD mediante una llamada a `RestoreScreenSaver` . Si una aplicación no usa la configuración del protector de pantalla del sistema, no tiene que llamar a este método o establecer la propiedad **DisableScreenSaver** .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



