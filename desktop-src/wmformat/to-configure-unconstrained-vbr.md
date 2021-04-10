---
title: Para configurar una VBR sin restricciones
description: Para configurar una VBR sin restricciones
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR sin restricciones
- velocidad de bits variable (VBR), configurar sin restricciones
- VBR (velocidad de bits variable), configurar sin restricciones
- perfiles, configuración de VBR sin restricciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149123"
---
# <a name="to-configure-unconstrained-vbr"></a>Para configurar una VBR sin restricciones

Puede usar la codificación de velocidad de bits variable (VBR) sin restricciones en una secuencia para especificar una velocidad de bits promedio que se mantendrá en el contenido codificado. La VBR sin restricciones difiere de los CBR normales en que la desviación en la velocidad de bits a lo largo del flujo puede ser mayor.

La velocidad de bits de la secuencia, establecida con [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), se usa como la velocidad de bits promedio deseada. Cuando se complete la codificación de la secuencia, puede usar [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) para recuperar dos propiedades adicionales: **g \_ wszVBRPeak** y **g \_ wszBufferAverage**. Estas propiedades describen la velocidad de bits máxima del contenido codificado y la ventana de búfer promedio del contenido, respectivamente.

La VBR sin restricciones debe utilizarse junto con la codificación de dos pasos. La codificación de dos pasos no está establecida en el perfil. Debe configurar el escritor para realizar un paso de preprocesamiento antes de escribir la secuencia. Para obtener más información sobre el uso de la codificación de dos pasos, consulte uso de la [codificación de Two-Pass](using-two-pass-encoding.md).

Para configurar una secuencia en un perfil que se va a codificar con VBR sin restricciones, realice los pasos siguientes:

1.  Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra un perfil existente al que desee agregar compatibilidad con VBR. Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).
3.  Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.
5.  Habilite la codificación VBR para la secuencia llamando a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la **propiedad \_ wszVBREnabled** .
6.  Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault:: SetProperty**.
7.  Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Guarde el perfil o páselo al objeto escritor.
9.  Configure el escritor para realizar un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




