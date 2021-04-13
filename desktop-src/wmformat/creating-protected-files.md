---
title: Crear archivos protegidos
description: Crear archivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- SDK de Windows Media Format, crear archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, crear archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358682"
---
# <a name="creating-protected-files"></a>Crear archivos protegidos

Para crear archivos de medios digitales protegidos mediante DRM versión 1 o DRM y versiones posteriores, vincule al archivo WMStubDRM. lib que obtuvo de Microsoft y cree el objeto de escritor. Para la protección de la versión 1, use la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) para establecer los atributos DRM que desea aplicar. Para las versiones 7 y posteriores, use los métodos de la interfaz [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .

En los temas siguientes se describe en detalle cómo proteger los archivos.

-   [Protección de archivos con DRM versión 1](protecting-files-with-drm-version-1.md)
-   [Protección de archivos con DRM versión 7 o posterior](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Versiones de DRM**](drm-versions.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Obtención de la biblioteca DRM necesaria**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Leer archivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




