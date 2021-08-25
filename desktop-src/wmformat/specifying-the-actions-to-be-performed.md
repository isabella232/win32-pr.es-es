---
title: Especificar las acciones que se realizarán
description: Especificar las acciones que se realizarán
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Formato de sistemas avanzados (ASF), especificar acciones
- ASF (formato de sistemas avanzados), especificar acciones
- administración de derechos digitales (DRM), especificar acciones
- DRM (administración de derechos digitales), especificar acciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d27df2904aee061deb252e08b59e1e88e4d1cd9e151290cd940fc48a650404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807805"
---
# <a name="specifying-the-actions-to-be-performed"></a>Especificar las acciones que se realizarán

Cuando se llama por primera vez a [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) para crear el objeto de lector, el segundo parámetro es un OR bit a bit **de** [**valores DE DERECHOS \_ DE WMT.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) Use este parámetro para especificar qué acciones realizará la aplicación en el primer archivo que se va a abrir. Estas acciones corresponden directamente a los derechos que se pueden especificar en la licencia. En las llamadas posteriores a [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), puede modificar los derechos que está solicitando llamando a [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), especificando la constante definida para la propiedad [**Drm \_ Rights**](drm-rights.md) y usando literales de cadena (de tipo **WCHAR)** separados por punto y coma para identificar los derechos. El fragmento de código siguiente solicita cuatro derechos: reproducir el archivo, copiarlo en un dispositivo y reproducirlo como parte de una lista de reproducción colaborativa.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> No confunda la propiedad Derechos de [**\_ DRM**](drm-rights.md) con la propiedad Marcas [**de \_ DRM,**](drm-flags.md) que es un **DWORD** que se usa para especificar qué derechos se deben aplicar a una licencia drm local de la versión 1 al copiar contenido de un CD.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




