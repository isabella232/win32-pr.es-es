---
description: Encoder-Specific del Registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570313"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific del Registro


Además de las entradas enumeradas anteriormente para el codificador, también debe registrar el codificador en la categoría de codificadores Windows Imaging Component (WIC) para que el motor de detección pueda encontrarlo. Para ello, realice las siguientes entradas del Registro. El primer GUID de las siguientes entradas es el identificador de categoría (CATID) para WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registro de un formato de contenedor con escritores de metadatos

Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del Registro para admitir los escritores de metadatos para los bloques de metadatos de las imágenes. Las entradas siguientes deben crearse en el identificador de clase (CLSID) del escritor de metadatos para cada formato de metadatos admitido en el formato de contenedor. Si el códec usa un contenedor Tagged Image File Format (TIFF), esta información ya está en el Registro y no es necesario crear estas entradas.

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

Si usa un formato de contenedor de estilo TIFF o jpeg, debe registrar una asociación entre el contenedor y ese formato de contenedor. Para obtener más información, vea la introducción en [Integración con Windows Galería de fotos y Windows Explorer](-wic-integrationregentries.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Entradas generales del Registro](-wic-generalregentries.md)
</dt> <dt>

[Entradas del Registro específicas del codificador](-wic-decoderregentries.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



