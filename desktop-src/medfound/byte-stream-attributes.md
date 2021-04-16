---
description: Atributos de secuencia de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de secuencia de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696181"
---
# <a name="byte-stream-attributes"></a>Atributos de secuencia de bytes

Los siguientes atributos se aplican a algunos flujos de bytes. Para averiguar si una secuencia de bytes admite atributos, consulte el objeto de flujo de bytes para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Atributo                                                                                  | Descripción                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**tipo de contenido de MF \_ BYTESTREAM \_ \_**](mf-bytestream-content-type-attribute.md)              | Especifica el tipo MIME de una secuencia de bytes.                         |
| [**\_duración de BYTESTREAM MF \_**](mf-bytestream-duration-attribute.md)                       | Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos. |
| [\_BYTESTREAM \_ \_ identificador URI de archivo IFO \_](mf-bytestream-ifo-file-uri.md)                           | Especifica la dirección URL de un archivo IFO asociado.                      |
| [**\_hora de \_ última \_ modificación \_ de MF BYTESTREAM**](mf-bytestream-last-modified-time-attribute.md) | Especifica cuándo se modificó por última vez una secuencia de bytes.                   |
| [**nombre del origen de MF \_ BYTESTREAM \_ \_**](mf-bytestream-origin-name-attribute.md)                | Especifica la dirección URL original de un flujo de bytes.                     |



 

Los siguientes atributos se aplican a los controladores de secuencias de bytes.



| Atributo                                                                                    | Descripción                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ acepta la \_ escritura de recursos compartidos \_](mf-bytestreamhandler-accepts-share-write.md) | Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso lo escriba. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



