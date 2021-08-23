---
title: Crear archivos protegidos
description: Crear archivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows SDK de formato multimedia, creación de archivos protegidos
- Windows SDK de formato multimedia, archivos protegidos
- Formato de sistemas avanzados (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Formato de sistemas avanzados (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Formato de sistemas avanzados (ASF),WMStubDRM.lib
- ASF (formato de sistemas avanzados),WMStubDRM.lib
- WMStubDRM.lib, crear archivos protegidos
- WMStubDRM.lib,archivos protegidos
- digital rights management (DRM),WMStubDRM.lib
- DRM (administración de derechos digitales),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809475"
---
# <a name="creating-protected-files"></a>Crear archivos protegidos

Para crear archivos multimedia digitales protegidos mediante DRM versión 1 o DRM versión 7 y posteriores, vincule al archivo WMStubDRM.lib que obtuvo de Microsoft y cree el objeto de escritor. Para la protección de la versión 1, use la [**interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) para establecer los atributos DRM que desea aplicar. Para las versiones 7 y posteriores, use los [**métodos de interfaz IWMDRMWriter.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)

En los temas siguientes se describe en detalle cómo proteger archivos.

-   [Protección de archivos con DRM versión 1](protecting-files-with-drm-version-1.md)
-   [Protección de archivos con DRM versión 7 o posterior](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> <dt>

[**Versiones de DRM**](drm-versions.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Obtención de la biblioteca DRM necesaria**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Leer archivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




