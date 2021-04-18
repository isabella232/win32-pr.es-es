---
description: Entradas generales del registro
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Entradas generales del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706623"
---
# <a name="general-registry-entries"></a>Entradas generales del registro


Las siguientes entradas del registro deben realizarse por separado para el descodificador y el codificador:

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

Se requieren las entradas FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions y Formats. Todos los demás son opcionales.

Tenga en cuenta que las entradas DeviceManufacturer y DeviceModels son específicas de los códecs sin formato y hacen referencia al fabricante de la cámara y a los modelos de cámara a los que se aplica el códec. La versión de la especificación es la versión de la especificación de formato de imagen con la que el códec es compatible. La entrada Formats especifica los formatos de píxel admitidos por el códec. Un códec puede admitir más de un formato de píxel. En ese caso, escribiría varias claves en \_ las clases HKEY \_ raíz \\ CLSID \\ {Encoder/descodificador CLSID} \\ formatos.

## <a name="arbitrationpriority"></a>ArbitrationPriority

A partir de Windows 8, ArbitrationPriority es una nueva entrada del registro. Los valores válidos son de 0 a 10. Cuando la clave ArbitrationPriority está presente, el valor de esta clave indicará a WIC que dé prioridad al códec asociado detrás de cualquier otro códec con un valor de ArbitrationPriority inferior. Esta evaluación se produce antes de que se produzca el arbitraje del códec de WIC existente, y garantiza que el códec asociado tiene prioridad por debajo de cualquier códec de la competencia, incluso si es igual o más capaz. Cualquier códec que no tenga un valor ArbitrationPriority explícito definido en el registro se establecerá de forma predeterminada en Priority 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Instalación y registro de CÓDECs](-wic-codecinstallandreg.md)
</dt> <dt>

[Entradas del registro específicas del codificador](-wic-encoderregentries.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Funcionamiento del componente de creación de imágenes de Windows: detección y arbitraje de códecs**](-wic-howwicworks.md)
</dt> </dl>

 

 



