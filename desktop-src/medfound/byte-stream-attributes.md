---
description: Atributos de flujo de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de flujo de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc6b6a73d58b3b5817f6c5654a4968c3f4677c0dca9ad4d184e93ee82d8206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959375"
---
# <a name="byte-stream-attributes"></a>Atributos de flujo de bytes

Los atributos siguientes se aplican a algunas secuencias de bytes. Para averiguar si una secuencia de bytes admite atributos, consulte el objeto de secuencia de bytes para la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| Atributo                                                                                  | Descripción                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**TIPO \_ DE CONTENIDO MF \_ \_ BYTESTREAM**](mf-bytestream-content-type-attribute.md)              | Especifica el tipo MIME de una secuencia de bytes.                         |
| [**DURACIÓN \_ DE BYTESTREAM \_ MF**](mf-bytestream-duration-attribute.md)                       | Especifica la duración de una secuencia de bytes, en unidades de 100 nanosegundos. |
| [\_URI DE ARCHIVO \_ IFO DE MF BYTESTREAM \_ \_](mf-bytestream-ifo-file-uri.md)                           | Especifica la dirección URL de un archivo IFO asociado.                      |
| [**HORA \_ DE ÚLTIMA MODIFICACIÓN \_ \_ DE \_ MF BYTESTREAM**](mf-bytestream-last-modified-time-attribute.md) | Especifica cuándo se modificó por última vez una secuencia de bytes.                   |
| [**NOMBRE \_ DE ORIGEN DE MF BYTESTREAM \_ \_**](mf-bytestream-origin-name-attribute.md)                | Especifica la dirección URL original de una secuencia de bytes.                     |



 

Los atributos siguientes se aplican a los controladores de flujo de bytes.



| Atributo                                                                                    | Descripción                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ ACEPTA ESCRITURA DE RECURSO \_ \_ COMPARTIDO](mf-bytestreamhandler-accepts-share-write.md) | Especifica si un controlador de secuencia de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



