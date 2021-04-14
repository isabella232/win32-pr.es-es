---
title: Aspectos básicos de DRM
description: Aspectos básicos de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- SDK de Windows Media Format, aspectos básicos de DRM
- Administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales), acerca de
- Administración de derechos digitales (DRM), protección de contenido
- DRM (administración de derechos digitales), protección de contenido
- Administración de derechos digitales (DRM), empaquetar contenido
- DRM (administración de derechos digitales), empaquetar contenido
- Administración de derechos digitales (DRM), lectura de contenido protegido
- DRM (administración de derechos digitales), lectura de contenido protegido
- protección de contenido
- empaquetado de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419137"
---
# <a name="drm-basics"></a>Aspectos básicos de DRM

Las tecnologías DRM de Windows Media son bastante sencillas desde la perspectiva del SDK de Windows Media Format. Los componentes del SDK se pueden usar para proteger el contenido y reproducir contenido protegido.

## <a name="protecting-content"></a>Proteger contenido

La protección del contenido (también conocido como contenido de empaquetado) implica el cifrado de la sección de datos del archivo y la inclusión de información en el encabezado del archivo que permite a los reproductores descifrar el contenido.

Para cifrar el contenido, se necesita una clave, que es un valor que se usa para inicializar los algoritmos de cifrado. Una clave se compone de dos partes: una inicialización de clave (o clave privada) y un identificador de clave (o clave pública). La inicialización de clave es el valor secreto con el que codificará el contenido. El identificador de clave es un valor público que se incluye en el encabezado de un archivo protegido.

Cuando un archivo está protegido, no se puede descifrar sin una licencia. Una licencia incluye información que especifica las condiciones de uso para el contenido protegido. El propietario del contenido decide los términos de una licencia y se puede personalizar para satisfacer diversas necesidades. Parte del proceso de empaquetado de un archivo consiste en incluir la dirección URL de una página web donde los usuarios pueden adquirir una licencia para obtener acceso al contenido.

## <a name="reading-protected-content"></a>Lectura de contenido protegido

Para leer contenido protegido, debe haber una licencia para el contenido en el equipo cliente. Las restricciones de licencia se comprueban internamente mediante los componentes de DRM del SDK de Windows Media Format, mientras que otras deben ser aplicadas por la aplicación.

Puede usar los objetos del SDK de Windows Media Format para ayudar al usuario a adquirir licencias para el contenido y realizar otras tareas administrativas, como actualizar componentes de DRM y realizar copias de seguridad de las licencias.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




