---
title: Leer archivos protegidos
description: Leer archivos protegidos
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- SDK de Windows Media Format, leer archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), leer archivos protegidos
- ASF (formato de sistemas avanzados), lectura de archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, leer archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788697"
---
# <a name="reading-protected-files"></a>Leer archivos protegidos

La lectura de un archivo o una secuencia de red protegida con DRM implica básicamente intentar abrir el archivo (o conectarse a la secuencia) y, a continuación, controlar los eventos que puedan enviarse desde los componentes de DRM.

Si un reproductor no es compatible con DRM (no se vincula a una biblioteca wmstubdrm. lib válida), se produce un error en la llamada a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) cuando intenta abrir un archivo protegido y devuelve el \_ contenido protegido de NS e \_ \_ o algún error relacionado.

Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido con DRM, el componente DRM busca automáticamente una licencia válida en el sistema local. Si se encuentra uno, el componente DRM descifra automáticamente el archivo de forma que sea completamente transparente para la aplicación. La acción que puede realizar una aplicación en el archivo descifrado depende de los derechos especificados en la licencia. Para obtener una descripción completa de los derechos posibles, consulte la documentación del SDK de Windows Media Rights Manager.

Si la aplicación no tiene una licencia válida para un archivo, el reproductor recibe una notificación de estado del componente DRM. A continuación, la aplicación de reproducción puede iniciar el proceso de [*adquisición de licencias*](wmformat-glossary.md) . Una vez recibida una licencia válida, se puede tener acceso al archivo. En las secciones siguientes se describen las tareas básicas que una aplicación debe realizar para implementar el proceso de adquisición de licencias:

-   [Especificar las acciones que se van a realizar](specifying-the-actions-to-be-performed.md)
-   [Control de eventos de adquisición de licencias](handling-license-acquisition-events.md)
-   [Individualización de aplicaciones DRM](individualizing-drm-applications.md)
-   [Control de eventos de individualización](handling-individualization-events.md)

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




