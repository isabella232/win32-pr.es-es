---
title: Versiones de DRM
description: Versiones de DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- SDK de Windows Media Format, versiones de DRM
- Administración de derechos digitales (DRM), versiones
- DRM (administración de derechos digitales), versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994085"
---
# <a name="drm-versions"></a>Versiones de DRM

Hay varias versiones de administración de derechos digitales (DRM) de Windows Media. La versión 1 de DRM suele estar separada de las otras versiones de esta documentación, ya que se implementa mediante técnicas que son diferentes de las versiones posteriores. La segunda generación de DRM de Windows Media se denomina DRM versión 7 porque se presentó como parte del SDK de Windows Media Format 7. A veces se denomina DRM versión 2. Las versiones posteriores de DRM de Windows Media, DRM versión 9 y el nuevo Windows Media DRM 10, son extensiones de la versión 7 de DRM y usan los mismos procedimientos para la implementación. Todas las versiones de Windows Media DRM usan las mismas rutinas de cifrado. las diferencias entre las versiones tienen que hacer con las características de licencia.

Al crear archivos protegidos con los objetos del SDK de Windows Media Format, debe admitir la versión 1 y la versión más reciente. Los archivos protegidos por la versión 1 de DRM se diferencian de los archivos protegidos por versiones posteriores solo en el contenido del encabezado. Los archivos más recientes que contienen la información de encabezado adicional se pueden seguir usando en clientes que solo representan contenido de la versión 1. Aunque las versiones posteriores de DRM ofrecen un mayor nivel de seguridad y características adicionales, hay todavía muchos reproductores que solo usan la versión 1.

Para obtener más información sobre las versiones de DRM, consulte la documentación del SDK de Windows Media Rights Manager.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




