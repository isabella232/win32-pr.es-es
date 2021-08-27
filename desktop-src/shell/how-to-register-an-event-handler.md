---
description: Un dispositivo puede generar potencialmente muchos eventos y cada evento tiene la opción de ser manipulado por uno de varios controladores diferentes.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Cómo registrar un controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090565"
---
# <a name="how-to-register-an-event-handler"></a>Cómo registrar un controlador de eventos

Un dispositivo puede generar potencialmente muchos eventos y cada evento tiene la opción de ser manipulado por uno de varios controladores diferentes. En Windows XP, se definen los siguientes eventos:

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>Instructions


Los controladores de eventos se definen en la **clave EventHandlers.** Los valores de una clave de controlador de eventos son los nombres de cada controlador que el usuario debe elegir cuando se detecta el evento. No hay ningún valor de datos asociado a estas entradas. A continuación se muestra una definición de ejemplo para un controlador de eventos personalizado llamado **MyNewRemovalEventHandler**, que presenta estas posibilidades de controlador al usuario:

-   Un controlador que se usará si el evento se detecta en un dispositivo realizado por la empresa llamada Contoso, Inc.
-   Controlador que se usará si el evento se detecta en un dispositivo creado por la empresa llamada Fabrikam, Inc.
-   Controlador que se usará en todos los demás casos.

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

Una vez definido un controlador de eventos, se debe registrar con un controlador de dispositivos para una de las posibilidades de evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval. MyNewRemovalEventHandler, definido anteriormente, se usa para DeviceRemoval en un controlador de dispositivo personalizado denominado MyDeviceHandler y se define para ese propósito en el ejemplo siguiente. De nuevo, el valor del Registro no tiene ningún componente de datos.

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
| PlayMusicFilesOnArrival  | Música archivos                                    |
| PlayVideoFilesOnArrival  | Archivos de vídeo                                    |
| PlayCDAudioOnArrival     | CD de audio (CD con formato REDBOOK con pistas de audio) |
| PlayDVDMovieOnArrival    | Películas de DVD                                     |



 

Windows Vista predefine el siguiente conjunto de EventHandlers además de los anteriores. 

| Clave EventHandlers              | Tipo de archivo o medio   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Películas de Super VideoCD |
| PlayVideoCDMovieOnArrival      | Películas de VideoCD       |



 

 

 



