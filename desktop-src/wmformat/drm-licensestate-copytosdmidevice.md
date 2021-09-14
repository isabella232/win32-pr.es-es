---
title: DRM_LicenseState_CopyToSDMIDevice
description: La propiedad \_ LicenseState \_ CopyToSDMIDevice de DRM contiene una estructura WM LICENSE STATE DATA que contiene detalles sobre cómo se ha aplicado este derecho \_ al \_ \_ contenido.
ms.assetid: 16d6748f-7998-4239-925d-d9d3952aab1b
keywords:
- DRM_LicenseState_CopyToSDMIDevice windows Media Format
topic_type:
- apiref
api_name:
- DRM_LicenseState_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e07974477bf7f265eef9a488e2bbfd8ddd0027
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360952"
---
# <a name="drm_licensestate_copytosdmidevice"></a>\_LicenseState \_ CopyToSDMIDevice de DRM

La **propiedad \_ LicenseState \_ CopyToSDMIDevice** de DRM contiene una estructura [**WM LICENSE STATE \_ \_ \_ DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) que contiene detalles sobre cómo se ha aplicado este derecho al contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice

## <a name="data-type"></a>Tipo de datos

**BINARIO DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 