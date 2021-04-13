---
title: Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11
description: Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Complementos de Windows Media Player, Asistente para complementos
- complementos, Asistente para complementos
- Complementos de procesamiento de señal digital, Asistente para complementos
- Complementos DSP, Asistente para complementos
- Asistente para complementos
- Visual Studio, Asistente para complementos de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420272"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11

El SDK de Windows Media Player 11 presenta los siguientes cambios en el Asistente para complementos de DSP:

-   Los complementos registran el modelo de subprocesos como "ambos". Esto permite que el complemento se ejecute en la canalización de Media Foundation en Windows Vista. Vea el archivo *projectname*. RGS.

    -   Los complementos de DSP de audio tienen compatibilidad con los dos formatos adicionales siguientes:

    <!-- -->

    -   \_formato Wave \_ IEEE \_ float
    -   \_Formato \_ de onda extensible con SUBformato KSDATAFORMAT \_ SubType \_ IEEE \_ float.

    Vea el archivo *projectname*. cpp.

    1.  Los complementos de DSP de vídeo admiten el formato de vídeo NV12.
    2.  Los complementos realizan llamadas adicionales a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) y [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: wmp \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Vea el archivo *projectnamedll*. cpp del proyecto.
    3.  Un proyecto adicional en cada solución crea un archivo DLL de proxy/stub para la interfaz personalizada de configuración de la página de propiedades. Vea el proyecto *projectnamePS* .
    4.  Las llamadas a métodos en desuso se han cambiado para usar las versiones más recientes.
    5.  El asistente puede generar un complemento de modo dual que funcione como DMO, implementando **IMediaObject** y como MFT, implementando **IMFTransform**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asistente para complementos de DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




