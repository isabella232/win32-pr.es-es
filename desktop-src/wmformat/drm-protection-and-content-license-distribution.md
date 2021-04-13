---
title: Protección de DRM y distribución de licencias de contenido
description: Protección de DRM y distribución de licencias de contenido
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- SDK de Windows Media Format, protección de contenido DRM
- SDK de Windows Media Format, licencias de DRM
- Advanced Systems Format (ASF), protección de contenido DRM
- ASF (formato de sistemas avanzados), protección de contenido DRM
- Advanced Systems Format (ASF), distribución de licencias de DRM
- ASF (formato de sistemas avanzados), distribución de licencias de DRM
- Administración de derechos digitales (DRM), protección de contenido
- DRM (administración de derechos digitales), protección de contenido
- Administración de derechos digitales (DRM), distribución de licencias
- DRM (administración de derechos digitales), distribución de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357744"
---
# <a name="drm-protection-and-content-license-distribution"></a>Protección de DRM y distribución de licencias de contenido

En el lado de la creación, la tecnología de administración de derechos digitales implica dos procesos principales: (1) protección del contenido y (2) proporcionar licencias para el contenido. La protección de un archivo básicamente implica el cifrado del contenido y la inclusión de una dirección URL en el encabezado del archivo que especifica dónde se puede obtener una licencia para el contenido. Si desea proteger los archivos con y, a continuación, distribuir los archivos a otros equipos o dispositivos, puede usar el SDK de Windows Media Format o el SDK de Windows Media Rights Manager para proteger el archivo. En escenarios Live-DRM, debe usar el SDK de Windows Media Format para proteger el contenido a medida que se codifica.

Para crear y emitir licencias para contenido protegido, puede crear su propia solución personalizada mediante los objetos del SDK de Windows Media Rights Manager, o puede usar un servicio ejecutado por terceros.

Sea cual sea el método que use, los archivos protegidos que cree contendrán, en el objeto de encabezado DRM, una dirección URL que indica a las aplicaciones cliente dónde obtener una licencia para el contenido.

> [!Note]  
> El SDK de Windows Media Format no proporciona compatibilidad para crear o emitir licencias.

 

En el lado de reproducción, una aplicación habilitada para DRM debe poder obtener licencias para el contenido protegido, descifrar el contenido con la clave incluida en la licencia y aplicar las restricciones de licencia, como el número de veces que se puede reproducir un archivo, o si el archivo se puede copiar en otro dispositivo. El SDK de Windows Media Format proporciona toda la compatibilidad necesaria para crear una aplicación de reproducción DRM totalmente habilitada.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




