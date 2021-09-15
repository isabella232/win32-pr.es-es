---
title: Actualizaciones del Asistente para complementos DSP para Reproductor de Windows Media 11
description: Actualizaciones del Asistente para complementos DSP para Reproductor de Windows Media 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Reproductor de Windows Media complementos, asistente para complementos
- complementos, asistente para complementos
- complementos de procesamiento de señales digitales, asistente para complementos
- Complementos de DSP, asistente para complementos
- Asistente para complementos
- Visual Studio,asistente para complementos DE DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465806"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Actualizaciones del Asistente para complementos DSP para Reproductor de Windows Media 11

El SDK Reproductor de Windows Media 11 presenta los siguientes cambios en el asistente para complementos de DSP:

-   Los complementos registran el modelo de subprocesos como "Ambos". Esto permite que el complemento se ejecute en la canalización Media Foundation en Windows Vista. Vea el *archivo projectname*.rgs.

    -   Los complementos DSP de audio admiten los dos formatos adicionales siguientes:

    <!-- -->

    -   FORMATO WAVE \_ \_ IEEE \_ FLOAT
    -   WAVE \_ FORMAT EXTENSIBLE con \_ subformato KSDATAFORMAT \_ SUBTYPE IEEE \_ \_ FLOAT.

    Consulte el *archivo projectname*.cpp.

    1.  Los complementos DSP de vídeo admiten el formato de vídeo NV12.
    2.  Los complementos hacen llamadas adicionales a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) con un nuevo tipo de complemento: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Consulte el archivo *.cpp projectnamedll* del proyecto.
    3.  Un proyecto adicional en cada solución crea un archivo DLL de proxy/stub para la interfaz personalizada de configuración de la página de propiedades. Consulte el *proyecto projectnamePS.*
    4.  Las llamadas a métodos en desuso se han cambiado para usar las versiones más recientes.
    5.  El asistente puede generar un complemento de modo dual que funcione como un DMO, mediante la implementación de **IMediaObject** y como MFT, mediante la implementación **de IMFTransform**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asistente para complementos DE DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




