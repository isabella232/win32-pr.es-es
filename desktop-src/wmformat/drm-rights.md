---
title: DRM_Rights
description: La \_ propiedad derechos DRM especifica los derechos que necesitará la aplicación en el siguiente intento de abrir un archivo protegido.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077296"
---
# <a name="drm_rights"></a>Derechos de DRM \_

La **propiedad \_ derechos DRM** especifica los derechos que necesitará la aplicación en el siguiente intento de abrir un archivo protegido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ derechos

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de lectura y escritura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) y se establece mediante [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

En la tabla siguiente se enumeran los derechos admitidos.



| Right                                           | Literal de cadena      | Descripción                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| copia de seguridad de g \_ wszWMDRM \_ derecha \_                      | "Backup"            | Derecho a realizar una copia de seguridad de la licencia.                                                                                                                                                                                        |
| g \_ wszWMDRM de colaboración de la \_ derecha \_ \_         | "CollaborativePlay" | Derecho para reproducir el archivo como parte de una lista de reproducción de colaboración.                                                                                                                                                          |
| g \_ wszWMDRM \_ \_ copia derecha                        | “Copiar”              | Derecho para copiar el archivo en un dispositivo. Este derecho sustituye a los derechos de copia anteriores (g \_ wszWMDRM la \_ \_ copia derecha \_ a \_ CD, g \_ wszWMDRM la \_ copia derecha a un \_ \_ \_ dispositivo que no es de \_ SDMI \_ y g \_ wszWMDRM \_ \_ copia derecha en el \_ \_ dispositivo de SDMI \_ ). |
| g \_ wszWMDRM \_ \_ copia derecha \_ a \_ CD                | "Print. Redbook"     | Derecho para copiar el archivo en un CD (formato de libro rojo). En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .<br/>                                                                             |
| g \_ wszWMDRM \_ la \_ copia derecha \_ en un \_ dispositivo que no es de \_ SDMI \_ | "Transfer. NONSDMI"  | Derecho para copiar el archivo en un dispositivo que no es de SDMI. En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .<br/>                                                                                  |
| g \_ wszWMDRM \_ la \_ copia derecha \_ en el dispositivo de \_ SDMI \_      | "Transfer. SDMI"     | Derecho para copiar el archivo en un dispositivo compatible con SDMI. En Windows Media DRM 10, este derecho se sustituye por la copia de la derecha de g \_ wszWMDRM \_ \_ .<br/>                                                                           |
| g \_ wszWMDRM \_ la \_ reproducción derecha                    | Reproducción              | Derecho para reproducir el archivo multimedia.                                                                                                                                                                                        |



 

Esta propiedad contiene una cadena de caracteres anchos de uno o más derechos separados por signos de punto y coma, por ejemplo: L "reproducción; Copiar CollaborativePlay".

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





