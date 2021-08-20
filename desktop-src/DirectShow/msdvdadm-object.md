---
description: Objeto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Objeto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072979"
---
# <a name="msdvdadm-object"></a>Objeto MSDVDAdm

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

> [!Note]  
> Esta API está en desuso. Para obtener información sobre la reproducción de DVD y la navegación en DirectShow, vea [Aplicaciones de DVD](dvd-applications.md).

 

Los métodos y propiedades del objeto "administration" permiten a una aplicación de scripting modificar su configuración predeterminada en el registro `MSDVDAdm` ® Windows® Microsoft. El Registro es una base de datos en todos los Windows en los que las aplicaciones pueden almacenar información sobre sí mismas para su uso durante la inicialización o durante el tiempo de ejecución.

La mayoría de estos métodos y propiedades no establecen ni recuperan los valores actuales en el [propio objeto MSWebDVD.](mswebdvd-object.md) Esto significa, por ejemplo, que cuando se llama a **GetParentalLevel,** el valor devuelto no es el nivel parental actual almacenado en el objeto . En su lugar, es el nivel parental predeterminado almacenado en el registro. Para obtener el nivel parental actual, llame al **método MSWebDVD** [**GetPlayerParentalLevel**](getplayerparentallevel-method.md). Al [**llamar a SaveParentalLevel,**](saveparentallevel-method.md) simplemente se escribe un nuevo nivel de acceso parental predeterminado en el registro. Todavía debe llamar al método **MSWebDVD** [**SelectParentalLevel**](selectparentallevel-method.md) para que el cambio suba inmediatamente en el **objeto MSWebDVD.** Los métodos de identificador de configuración regional (LCID) predeterminados funcionan de forma similar.

Por otro lado, los métodos [**BookmarkOnStop**](bookmarkonstop-property.md) y [**BookmarkOnClose**](bookmarkonclose-property.md) tienen efecto inmediatamente porque el objeto **MSWebDVD** comprueba esta configuración justo antes de que el usuario detenga la reproducción o cierre la aplicación, en lugar de durante la inicialización.

Se accede al `MSDVDAdm` objeto a través de la propiedad **DVDAdm** **de MSWebDVD.** Por ejemplo, si el objeto **MSWebDVD** se denomina "DVD", llame a **ChangePassword** como se muestra en el ejemplo de código siguiente.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Métodos y propiedades**

En la tabla siguiente se enumeran los métodos y propiedades expuestos por los métodos y propiedades del objeto MSDVDAdm.



| Método                                                          | Descripción                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Guarda una nueva contraseña de aplicación en el Registro.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Guarda un nuevo nivel parental predeterminado en el registro.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Guarda el nuevo país o región parental de la aplicación en el registro.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Comprueba si la contraseña especificada coincide con la contraseña guardada anteriormente.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera el nivel parental que se guardó por última vez en el registro.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera el país o región parental que se guardó por última vez en el registro.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Restaura la configuración del protector de pantalla del sistema.                                                                                                                                       |
| Propiedad                                                        | Descripción                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Activa o desactiva el protector de pantalla del sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para el flujo de subpicture.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para los menús.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario hace clic en el **botón** Detener. |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Establece o recupera un valor que indica al objeto MSDVDAdm si se debe guardar automáticamente un marcador de la ubicación y la configuración actuales cuando el usuario cierre la aplicación.     |



 

 

 



