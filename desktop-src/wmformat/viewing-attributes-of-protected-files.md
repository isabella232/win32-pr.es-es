---
title: Ver atributos de archivos protegidos
description: Ver atributos de archivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows SDK de formato multimedia, visualización de atributos de archivos protegidos
- Windows SDK de formato multimedia, atributos de archivos protegidos
- Windows SDK de formato multimedia, archivos protegidos
- Formato de sistemas avanzados (ASF), visualización de atributos de archivos protegidos
- ASF (formato de sistemas avanzados), visualización de atributos de archivos protegidos
- Formato de sistemas avanzados (ASF), atributos de archivos protegidos
- ASF (formato de sistemas avanzados), atributos de archivos protegidos
- Formato de sistemas avanzados (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- administración de derechos digitales (DRM), visualización de atributos de archivos protegidos
- DRM (administración de derechos digitales), visualización de atributos de archivos protegidos
- administración de derechos digitales (DRM), atributos de archivos protegidos
- DRM (administración de derechos digitales), atributos de archivos protegidos
- administración de derechos digitales (DRM), archivos protegidos
- DRM (administración de derechos digitales), archivos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256184"
---
# <a name="viewing-attributes-of-protected-files"></a>Ver atributos de archivos protegidos

En algunos escenarios, es posible que tenga que recuperar determinados atributos DRM en un archivo sin acceder realmente al contenido del archivo. Esta funcionalidad es útil, por ejemplo, en aplicaciones que procesan lotes de archivos de diferentes maneras en función de la información del encabezado de archivo. En versiones anteriores del SDK Windows Media Format, las aplicaciones tenían que vincularse a la biblioteca estática drm para abrir cualquier archivo protegido. Las aplicaciones que no tienen la biblioteca DRM pueden usar la interfaz [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) en el objeto del editor de metadatos para examinar determinados atributos DRM.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMEditor (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




