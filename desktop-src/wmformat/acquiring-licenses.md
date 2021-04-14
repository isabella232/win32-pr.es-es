---
title: Adquisición de licencias
description: Adquisición de licencias
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, adquisición de licencias
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), adquisición de licencias
- DRM (administración de derechos digitales), adquisición de licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias
- API extendidas del cliente, adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418391"
---
# <a name="acquiring-licenses"></a>Adquisición de licencias

Un escenario común para adquirir licencias es cuando un usuario tiene un archivo de Windows Media protegido e intenta tener acceso al contenido por primera vez. Dado que las API extendidas del cliente DRM de Windows Media son independientes de las rutinas de control de archivos ASF, el escenario de adquisición de licencias básico, aunque se admite, requiere más llamadas API que el SDK de Windows Media Format y el SDK de Media Foundation.

En esta sección se describe cómo usar las API extendidas del cliente DRM de Windows Media para adquirir licencias almacenadas en el almacén de licencias local en un equipo cliente. Contiene los temas siguientes.



| Tema                                                                | Descripción                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Adquisición de licencias silenciosa](silent-license-acquisition.md)         | Describe cómo adquirir licencias sin intervención del usuario.                                                                               |
| [Adquisición de licencias no silenciosa](non-silent-license-acquisition.md) | Describe cómo adquirir licencias cuando se requiere la intervención del usuario (por ejemplo, pagar por el contenido).                                     |
| [Entrega previa de licencias](license-pre-delivery.md)                     | Describe cómo extraer licencias de un servidor de licencias a un equipo cliente.                                                                 |
| [Crear licencias localmente](creating-licenses-locally.md)           | Describe cómo crear sus propias licencias sin descargarlas desde un servidor de licencias y cómo almacenarlas en el almacén de licencias local. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 




