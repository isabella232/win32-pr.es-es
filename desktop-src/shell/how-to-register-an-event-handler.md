---
description: Un dispositivo puede generar muchos eventos, y cada evento tiene la opción de ser administrado por uno de varios controladores diferentes.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Cómo registrar un controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985422"
---
# <a name="how-to-register-an-event-handler"></a>Cómo registrar un controlador de eventos

Un dispositivo puede generar muchos eventos, y cada evento tiene la opción de ser administrado por uno de varios controladores diferentes. En Windows XP, se definen los siguientes eventos:

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Instrucciones


Los controladores de eventos se definen en la clave **EventHandlers** . Los valores de una clave del controlador de eventos son los nombres de cada controlador que el usuario debe elegir cuando se detecte el evento. No hay ningún valor de datos asociado a estas entradas. A continuación se muestra una definición de ejemplo de un controlador de eventos personalizado denominado **MyNewRemovalEventHandler**, que presenta estas posibilidades de controlador al usuario:

-   Un controlador que se usará si el evento se detecta en un dispositivo realizado por la empresa llamada Contoso, Inc.
-   Un controlador que se usará si el evento se detecta en un dispositivo realizado por la empresa denominada Fabrikam, Inc.
-   Controlador que se va a usar en todos los demás casos.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

Una vez definido un controlador de eventos, se debe registrar con un controlador de dispositivo para una de las posibilidades de evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval. MyNewRemovalEventHandler, definido anteriormente, se usa para DeviceRemoval en un controlador de dispositivo personalizado denominado MyDeviceHandler y se define para ese propósito en el ejemplo siguiente. De nuevo, el valor del registro no tiene ningún componente de datos.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

Windows XP predefine el siguiente conjunto de EventHandlers. 

| Clave EventHandlers        | Tipo de archivo o medio                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | CD-R/CD-RW en blanco                               |
| ShowPicturesOnArrival    | Archivos de imagen                                  |
| PlayMusicFilesOnArrival  | Archivos de música                                    |
| PlayVideoFilesOnArrival  | Archivos de vídeo                                    |
| PlayCDAudioOnArrival     | CD de audio (formato REDBOOK CD con pistas de audio) |
| PlayDVDMovieOnArrival    | Películas de DVD                                     |



 

Windows Vista predefine el siguiente conjunto de EventHandlers, además de los anteriores. 

| Clave EventHandlers              | Tipo de archivo o medio   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Películas super VideoCD |
| PlayVideoCDMovieOnArrival      | Películas VideoCD       |



 

 

 



