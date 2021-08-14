---
title: Protección DRM y distribución de licencias de contenido
description: Protección DRM y distribución de licencias de contenido
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows SDK de formato multimedia, protección de contenido DRM
- Windows SDK de formato multimedia, licencias DRM
- Formato de sistemas avanzados (ASF), protección de contenido DRM
- ASF (formato de sistemas avanzados), protección de contenido DRM
- Formato de sistemas avanzados (ASF), distribución de licencias DRM
- ASF (formato de sistemas avanzados), distribución de licencias DRM
- administración de derechos digitales (DRM), protección de contenido
- DRM (administración de derechos digitales), protección de contenido
- administración de derechos digitales (DRM), distribución de licencias
- DRM (administración de derechos digitales), distribución de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704319"
---
# <a name="drm-protection-and-content-license-distribution"></a>Protección DRM y distribución de licencias de contenido

En el lado de la creación, la tecnología de administración de derechos digitales implica dos procesos principales: (1) proteger el contenido y (2) proporcionar licencias para el contenido. La protección de un archivo implica básicamente cifrar el contenido e incluir una dirección URL en el encabezado de archivo que especifica dónde se puede obtener una licencia para el contenido. Si desea proteger los archivos con y, a continuación, distribuirlos a otros equipos o dispositivos, puede usar el SDK de formato multimedia de Windows o el SDK de Windows Media Rights Manager para proteger el archivo. En escenarios de DRM en vivo, debe usar el SDK Windows Media Format para proteger el contenido a medida que se codifica.

Para crear y emitir licencias de contenido protegido, puede crear su propia solución personalizada mediante los objetos del SDK de Windows Media Rights Manager, o bien puede usar un servicio ejecutado por un tercero.

Sea cual sea el método que use, los archivos protegidos que cree contendrán, en el objeto de encabezado DRM, una dirección URL que indica a las aplicaciones cliente dónde obtener una licencia para el contenido.

> [!Note]  
> El SDK Windows Media Format no proporciona compatibilidad para crear o emitir licencias.

 

En el lado de la reproducción, una aplicación habilitada para DRM debe poder obtener licencias de contenido protegido, descifrar ese contenido mediante la clave contenida en la licencia y aplicar las restricciones de licencia, como el número de veces que se puede reproducir un archivo o si el archivo se puede copiar en otro dispositivo. El SDK Windows Media Format proporciona toda la compatibilidad necesaria para crear una aplicación de reproducción DRM totalmente habilitada.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




