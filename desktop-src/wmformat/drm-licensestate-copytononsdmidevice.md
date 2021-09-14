---
title: DRM_LicenseState_CopyToNonSDMIDevice
description: La propiedad \_ LicenseState \_ CopyToNonSDMIDevice de DRM contiene una estructura WM LICENSE STATE DATA que contiene detalles sobre cómo se ha aplicado este derecho \_ al \_ \_ contenido.
ms.assetid: aa0099b0-c6f8-4e27-a1f4-b98155d277aa
keywords:
- DRM_LicenseState_CopyToNonSDMIDevice windows Media Format
topic_type:
- apiref
api_name:
- DRM_LicenseState_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfebf4392ecffb6220b0eeda6e49e3c6ca89084c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360953"
---
# <a name="drm_licensestate_copytononsdmidevice"></a>\_LicenseState \_ copyToNonSDMIDevice de DRM

La **propiedad \_ LicenseState \_ CopyToNonSDMIDevice** de DRM contiene una estructura [**WM LICENSE STATE \_ \_ \_ DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) que contiene detalles sobre cómo se ha aplicado este derecho al contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice

## <a name="data-type"></a>Tipo de datos

**BINARIO DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 