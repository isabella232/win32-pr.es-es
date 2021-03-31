---
title: Ver atributos de archivos protegidos
description: Ver atributos de archivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- SDK de Windows Media Format, ver atributos de archivos protegidos
- SDK de Windows Media Format, atributos de archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), ver atributos de archivos protegidos
- ASF (formato de sistemas avanzados), ver atributos de archivos protegidos
- Advanced Systems Format (ASF), atributos de archivos protegidos
- ASF (formato de sistemas avanzados), atributos de archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Administración de derechos digitales (DRM), ver atributos de archivos protegidos
- DRM (administración de derechos digitales), ver atributos de archivos protegidos
- Administración de derechos digitales (DRM), atributos de archivos protegidos
- DRM (administración de derechos digitales), atributos de archivos protegidos
- Administración de derechos digitales (DRM), archivos protegidos
- DRM (administración de derechos digitales), archivos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788686"
---
# <a name="viewing-attributes-of-protected-files"></a>Ver atributos de archivos protegidos

En algunos escenarios, puede que necesite recuperar determinados atributos DRM en un archivo sin tener acceso realmente al contenido del archivo. Esta funcionalidad es útil, por ejemplo, en aplicaciones que procesan lotes de archivos de maneras diferentes en función de la información del encabezado de archivo. En versiones anteriores del SDK de Windows Media Format, las aplicaciones tenían que vincularse a la biblioteca estática de DRM para poder abrir cualquier archivo protegido. Las aplicaciones que no tienen la biblioteca DRM pueden utilizar la interfaz [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) en el objeto editor de metadatos para examinar determinados atributos DRM.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaz IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




