---
title: Para el uso de perfiles con Writer
description: Para el uso de perfiles con Writer
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows SDK de formato multimedia, escritura de archivos ASF
- Windows SDK de formato multimedia, creación de archivos ASF
- Windows SDK de formato multimedia, formato de sistemas avanzados (ASF)
- Formato de sistemas avanzados (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Formato de sistemas avanzados (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
- profiles,creating ASF files
- perfiles, escribir archivos ASF
- profiles,ASF file creation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0184469215dd109bcc4ca120e2db9cbead8b9bd250cb017456f9d7d08ea46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027273"
---
# <a name="to-use-profiles-with-the-writer"></a>Para el uso de perfiles con Writer

El escritor usa datos de perfil para crear archivos ASF. Debe especificar un perfil para su uso antes de hacer nada más con el escritor.

Puede establecer un perfil del sistema para usarlo con el escritor pasando el identificador de perfil al [**método IWMWriter::SetProfileByID.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)

Para especificar un perfil personalizado para usarlo con el escritor, debe obtener una interfaz [**IWMProfile**](iwmprofile.md) para un objeto que contenga los datos de perfil deseados. Para ello, puede usar uno de los métodos de carga de [**la interfaz IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Una vez que tenga una **interfaz IWMProfile** válida, puede pasar un puntero al método [**IWMWriter::SetProfile.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) Para obtener más información sobre la configuración del perfil, vea [Trabajar con perfiles.](working-with-profiles.md)

Si realiza cambios en el objeto de perfil mediante la interfaz **IWMProfile** después de establecer el perfil en el escritor, debe llamar de nuevo a **SetProfile** o, de lo contrario, los cambios no se reflejarán en el escritor. Sin embargo, al llamar **a SetProfile** se restablecerán todos los atributos de encabezado, así que asegúrese de establecer los atributos de encabezado necesarios después de llamar a este método.

La siguiente función de ejemplo establece el perfil en "Windows Media Video 8 for Dial-up Modems (56 Kbps)":


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
> No hay perfiles de sistema predefinidos que usen los códecs Windows media audio y vídeo de la serie 9. Para obtener más información, [vea Reusing Stream Configurations](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




