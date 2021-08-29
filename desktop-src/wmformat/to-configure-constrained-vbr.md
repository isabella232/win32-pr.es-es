---
title: Para configurar VBR restringido
description: Para configurar VBR restringido
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- streams,configuring VBR streams
- streams,velocidad de bits variable (VBR)
- velocidad de bits variable (VBR),streams
- VBR (velocidad de bits variable), secuencias
- streams,configuring constrained VBR
- velocidad de bits variable (VBR), configuración restringida
- VBR (velocidad de bits variable), configuración restringida
- profiles,configuring constrained VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d4f9546d67040bb5fb1aa5e43de34323679fe27aaf26826b57c3f0307c1181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929245"
---
# <a name="to-configure-constrained-vbr"></a>Para configurar VBR restringido

Puede usar la codificación de velocidad de bits variable restringida (VBR) en una secuencia para especificar una velocidad de bits media que se mantendrá en el contenido codificado. También se especifica la velocidad de bits máxima de la secuencia y la ventana de búfer máxima necesaria.

No puede saber cuál será la velocidad de bits media para una secuencia de VBR restringida antes de la codificación, pero puede usar una estimación aproximada. Como regla general, la velocidad de bits máxima que especifique terminará siendo de dos a tres veces la velocidad de bits media.

VBR restringido debe usarse junto con la codificación de dos pases. La codificación de dos pases no está establecida en el perfil. Debe configurar el sistema de escritura para que realice un paso de preprocesamiento antes de escribir la secuencia. Para obtener más información sobre el uso de la codificación de dos pases, vea [Using Two-Pass Encoding](using-two-pass-encoding.md).

Para configurar una secuencia en un perfil para que use la codificación VBR restringida, realice los pasos siguientes.

1.  Cree un objeto de administrador de perfiles mediante una llamada a [**la función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Abra un perfil existente al que desee agregar compatibilidad con VBR. Para obtener más información sobre cómo abrir perfiles, vea [Trabajar con perfiles.](working-with-profiles.md)
3.  Obtenga un objeto de configuración de flujo para el flujo que desea usar mediante una llamada a [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).
4.  Obtenga un puntero a la [**interfaz IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) del objeto de configuración de flujo mediante una llamada a **IWMStreamConfig::QueryInterface**.
5.  Habilite la codificación VBR para la secuencia mediante una llamada [**a IWMPropertyVault::SetProperty para**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) la **propiedad g \_ wszVBREnabled.**
6.  Use llamadas a **IWMPropertyVault::SetProperty** para establecer los valores máximos deseados para las propiedades **\_ g wszVBRBitrateMax** y **g \_ wszVBRBufferWindowMax.**
7.  Guarde los cambios realizados en la secuencia mediante una [**llamada a IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).
8.  Guarde el perfil o pásallo al objeto de escritor.
9.  Configure el sistema de escritura para realizar un paso de preprocesamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de vbr Secuencias**](configuring-vbr-streams.md)
</dt> </dl>

 

 




