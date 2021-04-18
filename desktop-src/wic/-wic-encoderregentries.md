---
description: Encoder-Specific entradas del registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific entradas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720600"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific entradas del registro


Además de las entradas indicadas anteriormente para el codificador, también debe registrar el codificador en la categoría de codificadores de componentes de imágenes de Windows (WIC) para que el motor de detección pueda encontrarlo. Para ello, realice las siguientes entradas del registro. El primer GUID en las siguientes entradas es el identificador de categoría (CATId) para WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrar un formato de contenedor con escritores de metadatos

Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del registro para admitir escritores de metadatos para los bloques de metadatos de las imágenes. Las siguientes entradas deben crearse en el identificador de clase (CLSID) del escritor de metadatos para cada formato de metadatos admitido en el formato del contenedor. Si el códec usa un contenedor de Tagged Image File Format (TIFF), esta información ya está en el registro y no es necesario crear estas entradas.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

Si usa un formato de contenedor de estilo TIFF o JPEG, debe registrar una asociación entre el contenedor y el formato del contenedor. Para obtener más información, consulte la introducción [a la integración con la Galería fotográfica de Windows y el explorador de Windows](-wic-integrationregentries.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Entradas generales del registro](-wic-generalregentries.md)
</dt> <dt>

[Entradas del registro específicas del codificador](-wic-decoderregentries.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



