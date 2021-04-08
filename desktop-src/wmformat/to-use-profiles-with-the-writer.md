---
title: Para el uso de perfiles con Writer
description: Para el uso de perfiles con Writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- SDK de Windows Media Format, escribir archivos ASF
- SDK de Windows Media Format, crear archivos ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Advanced Systems Format (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
- perfiles, crear archivos ASF
- perfiles, escribir archivos ASF
- perfiles, creación de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077437"
---
# <a name="to-use-profiles-with-the-writer"></a>Para el uso de perfiles con Writer

El escritor usa datos de perfil para crear archivos ASF. Debe especificar un perfil para usarlo antes de hacer nada más con el escritor.

Puede establecer un perfil del sistema para usarlo con el escritor pasando el ID. de perfil al método [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .

Para especificar un perfil personalizado para usarlo con el escritor, debe obtener una interfaz [**IWMProfile**](iwmprofile.md) para un objeto que contenga los datos de perfil deseados. Puede usar uno de los métodos de carga de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) para lograr esto. Una vez que tenga una interfaz **IWMProfile** válida, puede pasarle un puntero al método [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) . Para obtener más información acerca de la configuración del perfil, consulte [trabajar con perfiles](working-with-profiles.md).

Si realiza cambios en el objeto de perfil mediante la interfaz **IWMProfile** después de configurar el perfil en el escritor, debe llamar de nuevo a **SetProfile** o, de lo contrario, los cambios no se reflejarán en el escritor. Sin embargo, al llamar a **SetProfile** se restablecerán todos los atributos de encabezado, por lo que debe asegurarse de establecer los atributos de encabezado necesarios después de llamar a este método.

La siguiente función de ejemplo establece el perfil en "Windows Media Video 8 para módems de acceso telefónico (56 kbps)":


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> No hay ningún perfil de sistema predefinido que use los códecs de la serie Windows Media Audio y vídeo 9. Para obtener más información, vea [reutilizar las configuraciones de Stream](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




