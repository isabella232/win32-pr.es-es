---
title: DRM_DRMHeader_IndividualizedVersion
description: El atributo DRMHeaderIndividualizedVersion de DRM contiene la versión individualizada mínima \_ necesaria para reproducir el archivo.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion windows Media Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571256"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ DRMHeader \_ IndividualizedVersion

El **atributo \_ DRMHeaderIndividualizedVersion** de DRM contiene la versión individualizada mínima necesaria para reproducir el archivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Tipo de datos

**CADENA DE TIPO WMT \_ \_**

## <a name="remarks"></a>Observaciones

Este atributo solo está presente con contenido drm versión 7. Se puede recuperar con [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Para establecer la versión individualizada (también denominada versión de seguridad) en el archivo mediante [**IWMDRMWriter::SetDRMAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) debe usar la propiedad [**\_ IndividualizedVersion de DRM.**](drm-individualizedversion.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




