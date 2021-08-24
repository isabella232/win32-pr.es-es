---
title: Para configurar VBR sin restricciones
description: Para configurar VBR sin restricciones
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- streams,configuring VBR streams
- streams,velocidad de bits variable (VBR)
- velocidad de bits variable (VBR), secuencias
- VBR (velocidad de bits variable), secuencias
- streams,configuring unconstrained VBR
- velocidad de bits variable (VBR), configuración sin restricciones
- VBR (velocidad de bits variable), configurar sin restricciones
- profiles,configuring unconstrained VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff73a0aac8d13f015175080aac6eb580fc9686c67d892b14e4714746c8cea34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807765"
---
# <a name="to-configure-unconstrained-vbr"></a>Para configurar VBR sin restricciones

Puede usar la codificación de velocidad de bits variable (VBR) sin restricciones en una secuencia para especificar una velocidad de bits media que se mantendrá en el contenido codificado. VBR sin restricciones difiere del CBR normal en que la varianza en la velocidad de bits en toda la secuencia puede ser mayor.

La velocidad de bits de la secuencia, establecida con [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), se usa como la velocidad de bits media deseada. Una vez completada la codificación de la secuencia, puede usar [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) para recuperar dos propiedades adicionales: **g \_ wszVBRPeak** y **g \_ wszBufferAverage**. Estas propiedades describen la velocidad de bits máxima del contenido codificado y la ventana de búfer promedio del contenido, respectivamente.

VbR sin restricciones debe usarse junto con la codificación de dos pases. La codificación de dos pases no está establecida en el perfil. Debe configurar el sistema de escritura para que realice un paso de preprocesamiento antes de escribir la secuencia. Para obtener más información sobre el uso de la codificación de dos pasadas, vea [Using Two-Pass Encoding](using-two-pass-encoding.md).

Para configurar una secuencia en un perfil para codificarse con VBR sin restricciones, realice los pasos siguientes:

1.  Cree un objeto de administrador de perfiles mediante una llamada a [**la función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Abra un perfil existente al que desee agregar compatibilidad con VBR. Para obtener más información sobre cómo abrir perfiles, vea [Trabajar con perfiles.](working-with-profiles.md)
3.  Obtenga un objeto de configuración de flujo para el flujo que desea usar llamando a [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenga un puntero a la [**interfaz IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de flujo mediante una llamada a **IWMStreamConfig::QueryInterface**.
5.  Habilite la codificación VBR para la secuencia mediante una llamada [**a IWMPropertyVault::SetProperty para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) la **propiedad g \_ wszVBREnabled.**
6.  Establezca **g \_ wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax** en cero con **IWMPropertyVault::SetProperty**.
7.  Guarde los cambios realizados en la secuencia mediante una [**llamada a IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Guarde el perfil o pásallo al objeto de escritor.
9.  Configure el sistema de escritura para realizar un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de vbr Secuencias**](configuring-vbr-streams.md)
</dt> </dl>

 

 




