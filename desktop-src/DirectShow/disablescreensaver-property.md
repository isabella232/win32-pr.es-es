---
description: La propiedad DVDAdm. DisableScreenSaver activa o desactiva el protector de pantalla del sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propiedad DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906361"
---
# <a name="disablescreensaver-property"></a>Propiedad DisableScreenSaver

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm.DisableScreenSaver` propiedad activa o desactiva el protector de pantalla del sistema.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si la configuración del protector de pantalla del sistema está deshabilitada para la aplicación de reproducción de DVD; True significa que la configuración está deshabilitada.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y su valor predeterminado es true. Al ver un disco DVD-Video, un usuario no suele usar el mouse o el teclado durante largos períodos de tiempo. Por lo tanto, el control MSWebDVD de ActiveX® deshabilita el protector de pantalla del sistema de forma predeterminada. Object

## <a name="see-also"></a>Vea también

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



