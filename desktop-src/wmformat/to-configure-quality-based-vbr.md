---
title: Para configurar Quality-Based VBR
description: Para configurar Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- streams,configuring VBR streams
- streams,variable bit rate (VBR)
- velocidad de bits variable (VBR),streams
- VBR (velocidad de bits variable),streams
- streams,configuring quality-based VBR
- velocidad de bits variable (VBR), configuración basada en la calidad
- VBR (velocidad de bits variable), configuración basada en la calidad
- profiles,configuring quality-based VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466477"
---
# <a name="to-configure-quality-based-vbr"></a>Para configurar Quality-Based VBR

Puede usar la codificación de velocidad de bits variable (VBR) basada en calidad en una secuencia para especificar un nivel de calidad que se mantendrá para toda la secuencia, independientemente de los requisitos de velocidad de bits resultantes.

Para las secuencias de vídeo de VBR basadas en calidad, debe especificar un nivel de calidad de 1 a 100, con 100 que representen la calidad más alta. En la actualidad, solo hay 30 configuraciones de calidad discretas. Los siguientes niveles de calidad equivalen a la configuración de calidad discreta: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100. Los números entre dos valores consecutivos de la lista anterior equivalen a la misma configuración de calidad que el número inferior. Por ejemplo, se muestran 1 y 4, por lo que 2 y 3 tienen como resultado la misma configuración de calidad que 1.

En el caso de las secuencias de audio, puede enumerar los modos disponibles y recuperar un objeto de configuración de secuencia. Para obtener más información, vea [Para enumerar formatos de códec.](to-enumerate-codec-formats.md)

Al usar vídeo de VBR basado en calidad, debe establecer el **miembro dwBitrate** de la [**estructura WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) en un valor positivo. El escritor no usa este valor, pero pasar cero o un número negativo puede provocar errores al escribir.

Para configurar una secuencia en un perfil que se va a codificar con VBR basado en calidad, realice los pasos siguientes.

1.  Cree un objeto de administrador de perfiles mediante una llamada a [**la función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Abra un perfil existente al que quiera agregar compatibilidad con VBR. Para obtener más información sobre cómo abrir perfiles, vea [Trabajar con perfiles](working-with-profiles.md).
3.  Obtenga un objeto de configuración de secuencia para el flujo que desea usar llamando a [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenga un puntero a la [**interfaz IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de flujo llamando a **IWMStreamConfig::QueryInterface**.
5.  Habilite VBR para la secuencia mediante una llamada [**a IWMPropertyVault::SetProperty para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) la **propiedad g \_ wszVBREnabled.**
6.  Establezca el nivel de calidad de la secuencia de VBR llamando a **IWMPropertyVault::SetProperty para** la **propiedad g \_ wszVBRQuality.**
7.  Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault::SetProperty**.
8.  Guarde los cambios realizados en la secuencia llamando a [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
9.  Guarde el perfil o pásallo al objeto de escritor y empiece a escribir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




