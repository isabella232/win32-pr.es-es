---
title: Control de eventos de individualización
description: Control de eventos de individualización
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows SDK de formato multimedia, control de eventos de individualización
- Windows SDK de formato multimedia, eventos de individualización
- Formato de sistemas avanzados (ASF), control de eventos de individualización
- ASF (formato de sistemas avanzados), control de eventos de individualización
- Formato de sistemas avanzados (ASF), eventos de individualización
- ASF (formato de sistemas avanzados), eventos de individualización
- administración de derechos digitales (DRM), control de eventos de individualización
- DRM (administración de derechos digitales), control de eventos de individualización
- administración de derechos digitales (DRM), eventos de individualización
- DRM (administración de derechos digitales), eventos de individualización
- eventos de individualización
- events,individualization events
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433633"
---
# <a name="handling-individualization-events"></a>Control de eventos de individualización

Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido, el componente DRM examina el atributo [**\_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) de DRM en el archivo, que especifica el nivel de versión mínimo necesario para acceder al contenido. Todos los niveles del componente DRM funcionan con todas las versiones 7.0 y posteriores de Reproductor de Windows Media y el SDK Windows Media Format. Si el nivel de versión individualizada del componente DRM es inferior a la versión necesaria, el componente DRM enviará un evento **WMT \_ NEEDS \_ INDIVIDUALIZATION** al método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación. A continuación, la aplicación debe mostrar un mensaje o un cuadro de diálogo que pida a los usuarios que inicien o cancelen la actualización de seguridad. Este aviso es necesario porque, por motivos de privacidad, los usuarios deben conceder su permiso antes de instalar una actualización de seguridad en su equipo.

> [!Note]  
> El encabezado del contenido especifica solo los dos primeros dígitos para \_ DRMVersion \_ IndividualizedVersion de DRM. En otras palabras, para requerir un componente DRM de nivel 2.2.0.1, el encabezado contendrá "2.2".

 

Para iniciar la actualización de seguridad o desencadenar la individualización, llame al método [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con el parámetro *dwFlags* establecido en 1.

Debe controlar el evento **WMT \_ INDIVIDUALIZE** en la aplicación. El componente DRM desencadena este evento varias veces con el estado del proceso de individualización indicado en el *parámetro pValue,* que se convierte en un puntero a una estructura [**WM \_ INDIVIDUALIZE \_ STATUS.**](wm-individualize-status.md)

Una vez individualizado correctamente el componente DRM, la aplicación recibirá un evento **WMT \_ NO RIGHTS \_ \_ EX,** que indica que la aplicación ahora puede adquirir una licencia para el contenido.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos de adquisición de licencias**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualización de aplicaciones DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**IWMDRMReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




