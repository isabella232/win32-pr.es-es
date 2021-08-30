---
title: Adquisición de licencias
description: Adquisición de licencias
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows SDK de formato multimedia, API extendidas de cliente DRM
- Windows SDK de formato multimedia, API extendidas de cliente
- Windows SDK de formato multimedia, API extendidas
- Windows SDK de formato multimedia, API
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, adquisición de licencias
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- administración de derechos digitales (DRM), adquisición de licencias
- DRM (administración de derechos digitales), adquisición de licencias
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, adquisición de licencias
- API extendidas de cliente, adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e604db93561ac4e9b5e382436a4ec729e33890608d1dcb7c93cbe8372aa8898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089795"
---
# <a name="acquiring-licenses"></a>Adquisición de licencias

Un escenario común para adquirir licencias es cuando un usuario tiene un archivo Windows Media protegido e intenta acceder al contenido por primera vez. Dado que las API extendidas del cliente DRM de Windows Media son independientes de las rutinas de control de archivos de ASF, el escenario básico de adquisición de licencias, aunque se admite, requiere más llamadas API que usar el SDK de formato multimedia de Windows y el SDK de Media Foundation.

En esta sección se describe cómo usar las API extendidas de Windows Media DRM Client para adquirir licencias almacenadas en el almacén de licencias local en un equipo cliente. Contiene los temas siguientes.



| Tema                                                                | Descripción                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Adquisición silenciosa de licencias](silent-license-acquisition.md)         | Describe cómo adquirir licencias sin intervención del usuario.                                                                               |
| [Adquisición de licencias no silenciosas](non-silent-license-acquisition.md) | Describe cómo adquirir licencias cuando se requiere la intervención del usuario (por ejemplo, pagar por el contenido).                                     |
| [Entrega previa de licencias](license-pre-delivery.md)                     | Describe cómo extraer licencias de un servidor de licencias a un equipo cliente.                                                                 |
| [Crear licencias localmente](creating-licenses-locally.md)           | Describe cómo crear sus propias licencias sin descargarlas desde un servidor de licencias y cómo almacenarlas en el almacén de licencias local. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](drm-programming-guide.md)
</dt> </dl>

 

 




