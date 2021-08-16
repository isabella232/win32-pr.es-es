---
title: Aspectos básicos de DRM
description: Aspectos básicos de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows SDK de formato multimedia, conceptos básicos de DRM
- administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales),acerca de
- administración de derechos digitales (DRM), proteger el contenido
- DRM (administración de derechos digitales), protección de contenido
- administración de derechos digitales (DRM), empaquetado de contenido
- DRM (administración de derechos digitales), empaquetado de contenido
- administración de derechos digitales (DRM), lectura de contenido protegido
- DRM (administración de derechos digitales), lectura de contenido protegido
- proteger el contenido
- contenido de empaquetado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ef4439308868b0d77db1e9cefac7381fb8fd9ee78be50cccbf2a8dc26e4176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086145"
---
# <a name="drm-basics"></a>Aspectos básicos de DRM

Las Windows DRM multimedia son bastante sencillas desde la perspectiva del SDK Windows Media Format. Los componentes del SDK se pueden usar para proteger el contenido y reproducir contenido protegido.

## <a name="protecting-content"></a>Proteger contenido

Proteger el contenido (también denominado contenido de empaquetado) implica cifrar la sección de datos del archivo e incluir información en el encabezado de archivo que permite a los reproductores descifrar el contenido.

Para cifrar el contenido, necesita una clave, que es un valor que se usa para seeder los algoritmos de cifrado. Una clave se forma de dos partes: una ed.ed de clave (o clave privada) y un identificador de clave (o clave pública). La edificación de clave es el valor secreto con el que codifica el contenido. El identificador de clave es un valor público que se incluye en el encabezado de un archivo protegido.

Cuando un archivo está protegido, no se puede descifrar sin una licencia. Una licencia incluye información que especifica los términos de uso del contenido protegido. El propietario del contenido decide los términos de una licencia y se pueden personalizar para satisfacer una variedad de necesidades. Parte del proceso de empaquetado de un archivo es incluir la dirección URL de una página web en la que los usuarios pueden adquirir una licencia para acceder al contenido.

## <a name="reading-protected-content"></a>Leer contenido protegido

Para leer contenido protegido, una licencia para el contenido debe residir en el equipo cliente. Algunos componentes drm del SDK de formato multimedia de Windows comprueban internamente algunas restricciones de licencia, mientras que la aplicación debe aplicar otras.

Puede usar los objetos del SDK de formato multimedia de Windows para ayudar al usuario a adquirir licencias de contenido y realizar otras tareas administrativas, como actualizar componentes DRM y realizar una copia de seguridad de licencias.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




