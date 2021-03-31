---
title: Para configurar una VBR restringida
description: Para configurar una VBR restringida
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flujos, configurar secuencias VBR
- secuencias, velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- flujos, configurar VBR restringida
- velocidad de bits variable (VBR), configurar restricciones
- VBR (velocidad de bits variable), configurar restricciones
- perfiles, configuración de VBR restringida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077440"
---
# <a name="to-configure-constrained-vbr"></a>Para configurar una VBR restringida

Puede usar la codificación de velocidad de bits variable (VBR) restringida en una secuencia para especificar una velocidad de bits promedio que se mantendrá en el contenido codificado. También se especifica la velocidad de bits máxima de la secuencia y la ventana de búfer máxima requerida.

No se puede saber cuál será la velocidad de bits media de una secuencia VBR restringida antes de la codificación, pero se puede usar una estimación aproximada. Como norma general, la velocidad de bits máxima que especifique terminará siendo de dos a tres veces la velocidad de bits promedio.

La VBR restringida debe usarse junto con la codificación de dos pasos. La codificación de dos pasos no está establecida en el perfil. Debe configurar el escritor para realizar un paso de preprocesamiento antes de escribir la secuencia. Para obtener más información sobre el uso de la codificación de dos pasos, consulte uso de la [codificación de Two-Pass](using-two-pass-encoding.md).

Para configurar una secuencia en un perfil para usar la codificación VBR restringida, realice los pasos siguientes.

1.  Cree un objeto de administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Abra un perfil existente al que desee agregar compatibilidad con VBR. Para obtener más información acerca de la apertura de perfiles, consulte [trabajar con perfiles](working-with-profiles.md).
3.  Obtenga un objeto de configuración de secuencia para la secuencia que desea usar llamando a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtiene un puntero a la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.
5.  Habilite la codificación VBR para la secuencia llamando a [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para la **propiedad \_ wszVBREnabled** .
6.  Use llamadas a **IWMPropertyVault:: SetProperty** para establecer los valores máximos deseados para las propiedades **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** .
7.  Guarde los cambios realizados en la secuencia mediante una llamada a [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Guarde el perfil o páselo al objeto escritor.
9.  Configure el escritor para realizar un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias VBR**](configuring-vbr-streams.md)
</dt> </dl>

 

 




