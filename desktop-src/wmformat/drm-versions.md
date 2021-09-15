---
title: Versiones de DRM
description: Versiones de DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows SDK de formato multimedia, versiones de DRM
- administración de derechos digitales (DRM),versiones
- DRM (administración de derechos digitales),versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570241"
---
# <a name="drm-versions"></a>Versiones de DRM

Hay varias versiones de Windows Administración de derechos digitales multimedia (DRM). La versión 1 de DRM se suele diferenciar de las demás versiones de esta documentación, ya que se implementa mediante técnicas que son diferentes de las versiones posteriores. La segunda generación de Windows DRM multimedia se denomina DRM versión 7 porque se introdujo como parte del SDK Windows Media Format 7. A veces se denomina DRM versión 2. Las versiones posteriores de Windows Media DRM, DRM versión 9 y el nuevo DRM multimedia de Windows 10, son extensiones de DRM versión 7 y usan los mismos procedimientos para la implementación. Todas las versiones de Windows DRM multimedia usan las mismas rutinas de cifrado; las diferencias entre las versiones tienen que ver con las características de licencia.

Al crear archivos protegidos mediante los objetos del SDK Windows Media Format, debe admitir tanto la versión 1 como la versión más reciente. Los archivos protegidos por DRM versión 1 difieren de los archivos protegidos por versiones posteriores solo en el contenido del encabezado. Los archivos más recientes que contienen la información de encabezado adicional todavía se pueden usar en clientes que representan solo el contenido de la versión 1. Aunque las versiones posteriores de DRM ofrecen un mayor nivel de seguridad y características adicionales, todavía hay muchos reproductores que solo usan la versión 1.

Para más información sobre las versiones de DRM, consulte la Windows del SDK de Media Rights Manager.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




