---
title: DRM_Rights
description: La propiedad Derechos de DRM especifica los derechos que la \_ aplicación necesitará en el siguiente intento de abrir un archivo protegido.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights windows Media Format
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d655ea3f4a0a5dccc8b5e1380296948c9a55dce1d86336f824b30189f6557d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930905"
---
# <a name="drm_rights"></a>Derechos de \_ DRM

La **propiedad \_ Derechos** de DRM especifica los derechos que la aplicación necesitará en el siguiente intento de abrir un archivo protegido.

## <a name="global-constant"></a>Constante global

g \_ wszWMDRM \_ Rights

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

Se trata de una propiedad de lectura y escritura que se recupera mediante [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) y se establece mediante [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

En la tabla siguiente se enumeran los derechos admitidos.



| Right                                           | Literal de cadena      | Descripción                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ RIGHT \_ BACKUP                      | "Backup"            | Derecho para hacer una copia de seguridad de la licencia.                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT COLLABORATIVE \_ \_ PLAY         | "CollaborativePlay" | Derecho a reproducir el archivo como parte de una lista de reproducción colaborativa.                                                                                                                                                          |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | “Copiar”              | Derecho para copiar el archivo en un dispositivo. Este derecho sustituye a los derechos de copia anteriores (g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD, g \_ wszWMDRM RIGHT COPY TO NON SDMI DEVICE y \_ g \_ \_ \_ \_ \_ \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE). |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD                | "Print.redbook"     | Derecho para copiar el archivo en un CD (formato de libro rojo). En Windows DRM multimedia 10, este derecho se reemplaza por g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                             |
| g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE | "Transfer.NONSDMI"  | Derecho para copiar el archivo en un dispositivo que no es SDMI. En Windows Drm multimedia 10, este derecho se reemplaza por g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                                  |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE      | "Transfer.SDMI"     | Derecho para copiar el archivo en un dispositivo compatible con SDMI. En Windows DRM multimedia 10, este derecho se reemplaza por g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                           |
| g \_ wszWMDRM \_ RIGHT \_ PLAYBACK                    | "Reproducir"              | Derecho para reproducir el archivo multimedia.                                                                                                                                                                                        |



 

Esta propiedad contiene una cadena de caracteres anchos de uno o varios derechos separados por punto y coma, por ejemplo: L"Playback; Copy; CollaborativePlay".

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de DRM**](drm-properties.md)
</dt> </dl>

 

 





