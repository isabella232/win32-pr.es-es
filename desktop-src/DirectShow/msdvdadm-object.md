---
description: Objeto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Objeto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193d5e46837c576c61b8bf1704ec967c1b6fc246
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151987"
---
# <a name="msdvdadm-object"></a>Objeto MSDVDAdm

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

> [!Note]  
> Esta API está en desuso. Para obtener información acerca de la reproducción de DVD y la navegación en DirectShow, consulte [aplicaciones de DVD](dvd-applications.md).

 

Los métodos y las propiedades del `MSDVDAdm` objeto "Administration" permiten que una aplicación de scripting modifique su configuración predeterminada en el registro de Microsoft® Windows®. El registro es una base de datos de todos los sistemas de Windows donde las aplicaciones pueden almacenar información sobre ellos mismos para su uso en la inicialización o durante el tiempo de ejecución.

La mayoría de estos métodos y propiedades no establecen ni recuperan los valores actuales en el propio objeto [MSWebDVD](mswebdvd-object.md) . Esto significa, por ejemplo, que al llamar a **GetParentalLevel** , el valor devuelto no es el nivel parental actual almacenado en el objeto. En su lugar, es el nivel parental predeterminado almacenado en el registro. Para obtener el nivel parental actual, llame al método **MSWebDVD** [**GetPlayerParentalLevel**](getplayerparentallevel-method.md). La llamada a [**SaveParentalLevel**](saveparentallevel-method.md) simplemente escribe un nuevo nivel de acceso parental predeterminado en el registro; todavía es necesario llamar al método **MSWebDVD** [**SelectParentalLevel**](selectparentallevel-method.md) para que el cambio surta efecto inmediatamente en el objeto **MSWebDVD** . Los métodos de identificador de configuración regional (LCID) predeterminados funcionan de forma similar.

Por otro lado, los métodos [**BookmarkOnStop**](bookmarkonstop-property.md) y [**BookmarkOnClose**](bookmarkonclose-property.md) surten efecto inmediatamente porque el objeto **MSWebDVD** comprueba estos valores justo antes de que el usuario detenga la reproducción o cierre la aplicación, en lugar de durante la inicialización.

Tiene acceso al `MSDVDAdm` objeto a través de la propiedad **DVDAdm** de **MSWebDVD**. Por lo tanto, por ejemplo, si el objeto **MSWebDVD** se denomina "DVD", llame a **ChangePassword** como se muestra en el ejemplo de código siguiente.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Métodos y propiedades**

En la tabla siguiente se enumeran los métodos y las propiedades que exponen los métodos y las propiedades del objeto MSDVDAdm.



| Método                                                          | Descripción                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Guarda una nueva contraseña de aplicación en el registro.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Guarda un nuevo nivel primario predeterminado en el registro.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Guarda el nuevo país o región parental de la aplicación en el registro.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Comprueba si la contraseña especificada coincide con la contraseña guardada previamente.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera el nivel parental que se guardó por última vez en el registro.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera el país o la región parental que se guardó por última vez en el registro.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Restaura la configuración del protector de pantalla del sistema.                                                                                                                                       |
| Propiedad                                                        | Descripción                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Activa o desactiva el protector de pantalla del sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de subimagen.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para los menús.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Establece o recupera un valor que indica al objeto MSDVDAdm si se va a guardar automáticamente un marcador de la ubicación actual y la configuración cuando el usuario haga clic en el botón **detener** . |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la configuración y la ubicación actuales cuando el usuario cierra la aplicación.     |



 

 

 



