---
title: Especificar las acciones que se van a realizar
description: Especificar las acciones que se van a realizar
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- Advanced Systems Format (ASF), especificar acciones
- ASF (formato de sistemas avanzados), especificación de acciones
- Administración de derechos digitales (DRM), especificación de acciones
- DRM (administración de derechos digitales), especificación de acciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420297"
---
# <a name="specifying-the-actions-to-be-performed"></a>Especificar las acciones que se van a realizar

La primera vez que se llama a [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) para crear el objeto de lector, el segundo parámetro es **una operación OR bit a bit** de los valores de los [**\_ derechos de WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) . Use este parámetro para especificar las acciones que realizará la aplicación en el primer archivo que se va a abrir. Estas acciones se corresponden directamente con los derechos que se pueden especificar en la licencia. En las llamadas subsiguientes a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), puede modificar los derechos que está solicitando llamando a [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), especificando la constante definida para la propiedad [**\_ derechos DRM**](drm-rights.md) y usando literales de cadena (de tipo **WCHAR**) separados por punto y coma para identificar los derechos. El fragmento de código siguiente solicita cuatro derechos: reproducir el archivo, copiarlo en un dispositivo y reproducirlo como parte de una lista de reproducción colaborativa.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> No confunda la propiedad [**\_ derechos DRM**](drm-rights.md) con la propiedad [**\_ marcas DRM**](drm-flags.md) , que es un **valor DWORD** que se usa para especificar los derechos que se aplicarán a una licencia local de DRM versión 1 al copiar contenido desde un CD.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




