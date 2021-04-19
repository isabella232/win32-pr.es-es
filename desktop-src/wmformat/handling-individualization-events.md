---
title: Control de eventos de individualización
description: Control de eventos de individualización
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- SDK de Windows Media Format, control de eventos de individualización
- SDK de Windows Media Format, eventos de individualización
- Advanced Systems Format (ASF), control de eventos de individualización
- ASF (formato de sistemas avanzados), control de eventos de individualización
- Advanced Systems Format (ASF), eventos de individualización
- ASF (formato de sistemas avanzados), eventos de individualización
- Administración de derechos digitales (DRM), control de eventos de individualización
- DRM (administración de derechos digitales), control de eventos de individualización
- Administración de derechos digitales (DRM), eventos de individualización
- DRM (administración de derechos digitales), eventos de individualización
- eventos de individualización
- eventos, eventos de individualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695543"
---
# <a name="handling-individualization-events"></a>Control de eventos de individualización

Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido, el componente DRM examina el atributo [**\_ \_ IndividualizedVersion de DRM DRMHeader**](drm-drmheader-individualizedversion.md) en el archivo, que especifica el nivel de versión mínimo necesario para tener acceso al contenido. Todos los niveles del componente DRM funcionan con todas las versiones 7,0 y posteriores de Windows Media Player y el SDK de Windows Media Format. Si el nivel de versión individualizado del componente DRM es inferior a la versión requerida, el componente DRM enviará un evento **WMT necesitará un evento de \_ \_ individualización** al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación. A continuación, la aplicación debe mostrar un mensaje o un cuadro de diálogo que solicite a los usuarios que inicien o cancelen la actualización de seguridad. Este mensaje es necesario porque, por motivos de privacidad, los usuarios deben conceder su permiso antes de instalar una actualización de seguridad en su equipo.

> [!Note]  
> El encabezado del contenido especifica solo los dos primeros dígitos para DRM \_ DRMVersion \_ IndividualizedVersion. En otras palabras, para requerir un componente 2.2.0.1 de DRM de nivel, el encabezado contendría "2,2".

 

Para iniciar la actualización de seguridad y/o desencadenar la individualización, llame al método [**IWMDRMReader:: individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con el parámetro *dwFlags* establecido en 1.

Debe controlar el evento **WMT \_ individual** en la aplicación. Este evento se activará varias veces mediante el componente DRM con el estado del proceso de individualización indicado en el parámetro *pValue* , que se convierte en un puntero a una estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de la función de la función de usuario.

Una vez que el componente DRM se haya individualizado correctamente, la aplicación recibirá un evento **WMT \_ no \_ Rights \_ ex** , lo que indica que la aplicación ahora puede continuar para adquirir una licencia para el contenido.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos de adquisición de licencias**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualización de aplicaciones DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**Interfaz IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




