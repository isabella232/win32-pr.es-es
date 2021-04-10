---
title: Para configurar Quality-Based VBR
description: Para configurar Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR basada en la calidad
- velocidad de bits variable (VBR), configurar basado en la calidad
- VBR (velocidad de bits variable), configuración basada en la calidad
- perfiles, configuración de VBR basada en la calidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995020"
---
# <a name="to-configure-quality-based-vbr"></a>Para configurar Quality-Based VBR

Puede usar la codificación de velocidad de bits variable (VBR) basada en la calidad en una secuencia para especificar un nivel de calidad que se mantendrá para todo el flujo, independientemente de los requisitos de velocidad de bits que resulten.

En el caso de las secuencias de vídeo VBR basadas en la calidad, debe especificar un nivel de calidad de 1 a 100, con 100 que representa la calidad más alta. En la actualidad, solo hay 30 valores de calidad discretos. Los siguientes niveles de calidad son equivalentes a los valores de calidad discretos: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. Los números entre dos valores consecutivos de la lista anterior equivalen a la misma configuración de calidad que el número inferior. Por ejemplo, 1 y 4 se enumeran, por lo que 2 y 3 dan como resultado la misma configuración de calidad que 1.

En el caso de las secuencias de audio, puede enumerar los modos disponibles y recuperar un objeto de configuración de la secuencia. Para obtener más información, vea [para enumerar los formatos de códec](to-enumerate-codec-formats.md).

Al usar el vídeo VBR basado en la calidad, debe establecer el miembro **dwBitrate** de la estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) en un valor positivo. El escritor no usa este valor, pero si se pasa cero o un número negativo, se pueden producir errores al escribir.

Para configurar una secuencia en un perfil que se va a codificar con VBR basada en la calidad, realice los pasos siguientes.

1.  Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra un perfil existente al que desee agregar compatibilidad con VBR. Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).
3.  Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.
5.  Habilite VBR para la secuencia mediante una llamada a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la propiedad **\_ wszVBREnabled** .
6.  Establezca el nivel de calidad de la secuencia VBR llamando a **IWMPropertyVault:: SetProperty** para la propiedad **\_ wszVBRQuality** .
7.  Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault:: SetProperty**.
8.  Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Guarde el perfil o páselo al objeto escritor y empiece a escribir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




