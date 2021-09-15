---
description: Requisitos de recursos
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Requisitos de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572088"
---
# <a name="requirements-for-resources"></a>Requisitos de recursos

Windows Dispositivos portátiles define las siguientes categorías de recursos como **valores PROPERTYKEY.** Estos valores se usan para describir recursos individuales en un objeto . El *miembro pid* de la clave de propiedad puede ser diferente para describir distintos recursos del mismo tipo para todos los tipos excepto **WPD RESOURCE \_ \_ DEFAULT,** que solo puede describir un recurso. En la página de descripción vinculada de cada tipo de recurso se enumeran los atributos admitidos por ese recurso.



| Resource PROPERTYKEY                                                | Descripción                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**WPD \_ RESOURCE \_ DEFAULT**](wpd-resource-default.md)              | Especifica el archivo completo detrás del objeto . Este es el único recurso necesario para cualquier objeto con un recurso. |
| [**WPD \_ RESOURCE \_ ALBUM \_ ART**](wpd-resource-album-art.md)         | Especifica una imagen que representa las ilustraciones del álbum para el objeto .                                           |
| [**CLIP DE \_ AUDIO DE RECURSOS \_ WPD \_**](wpd-resource-audio-clip.md)       | Especifica un clip de audio para el objeto .                                                                        |
| [**WPD \_ RESOURCE \_ CONTACT \_ PHOTO**](wpd-resource-contact-photo.md) | Especifica una imagen que representa una foto del individuo al que se hace referencia en el objeto de contacto.                |
| [**WPD \_ RESOURCE \_ GENERIC**](wpd-resource-generic.md)              | Recurso genérico de tipo de datos sin definir. Esto debe tratarse como una matriz de bytes.                             |
| [**ICONO DE RECURSO DE WPD \_ \_**](wpd-resource-icon.md)                    | Un icono.                                                                                                       |
| [**MINIATURA DE RECURSOS DE WPD \_ \_**](wpd-resource-thumbnail.md)          | Una imagen en miniatura.                                                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 



