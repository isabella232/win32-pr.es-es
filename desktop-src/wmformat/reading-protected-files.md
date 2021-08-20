---
title: Leer archivos protegidos
description: Leer archivos protegidos
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows SDK de formato multimedia, lectura de archivos protegidos
- Windows SDK de formato multimedia, archivos protegidos
- Formato de sistemas avanzados (ASF), lectura de archivos protegidos
- ASF (formato de sistemas avanzados), leer archivos protegidos
- Formato de sistemas avanzados (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Formato de sistemas avanzados (ASF),WMStubDRM.lib
- ASF (formato de sistemas avanzados),WMStubDRM.lib
- WMStubDRM.lib, leer archivos protegidos
- WMStubDRM.lib,archivos protegidos
- administración de derechos digitales (DRM),WMStubDRM.lib
- DRM (administración de derechos digitales),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c700629fd66fdf0aa8bb1ff837b968232cf9301c39b951dd0a74678c9f1312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846106"
---
# <a name="reading-protected-files"></a>Leer archivos protegidos

Leer un archivo protegido con DRM o una secuencia de red básicamente implica intentar abrir el archivo (o conectarse a la secuencia) y, a continuación, controlar los eventos que se puedan enviar desde los componentes de DRM.

Si un reproductor no está habilitado para DRM (no vincula a una biblioteca wmstubdrm.lib válida), se produce un error en la llamada [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) cuando intenta abrir un archivo protegido y devuelve CONTENIDO PROTEGIDO de NS E o algún \_ \_ error \_ relacionado.

Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido con DRM, el componente DRM busca automáticamente una licencia válida en el sistema local. Si se encuentra uno, el componente DRM descifra automáticamente el archivo de una manera completamente transparente para la aplicación. La acción que puede realizar una aplicación en el archivo descifrado depende de los derechos especificados en la licencia. Para obtener una descripción completa de los posibles derechos, consulte la Windows del SDK de Media Rights Manager.

Si la aplicación no tiene una licencia válida para un archivo, el reproductor recibe una notificación de estado del componente DRM. A continuación, la aplicación player puede iniciar el [*proceso de adquisición de*](wmformat-glossary.md) licencias. Una vez recibida una licencia válida, se puede acceder al archivo. En las secciones siguientes se describen las tareas básicas que una aplicación debe realizar al implementar el proceso de adquisición de licencias:

-   [Especificar las acciones que se realizarán](specifying-the-actions-to-be-performed.md)
-   [Control de eventos de adquisición de licencias](handling-license-acquisition-events.md)
-   [Individualización de aplicaciones DRM](individualizing-drm-applications.md)
-   [Control de eventos de individualización](handling-individualization-events.md)

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




