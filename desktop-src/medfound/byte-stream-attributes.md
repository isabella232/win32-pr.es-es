---
description: Atributos de flujo de bytes
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Atributos de flujo de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241178"
---
# <a name="byte-stream-attributes"></a>Atributos de flujo de bytes

Los siguientes atributos se aplican a algunas secuencias de bytes. Para averiguar si una secuencia de bytes admite atributos, consulte el objeto de flujo de bytes para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| Atributo                                                                                  | Descripción                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**TIPO \_ DE CONTENIDO MF \_ \_ BYTESTREAM**](mf-bytestream-content-type-attribute.md)              | Especifica el tipo MIME de una secuencia de bytes.                         |
| [**DURACIÓN \_ DE BYTESTREAM \_ DE MF**](mf-bytestream-duration-attribute.md)                       | Especifica la duración de una secuencia de bytes, en unidades de 100 nanosegundos. |
| [\_URI DE ARCHIVO \_ IFO DE MF BYTESTREAM \_ \_](mf-bytestream-ifo-file-uri.md)                           | Especifica la dirección URL de un archivo IFO asociado.                      |
| [**HORA DE ÚLTIMA MODIFICACIÓN DE MF \_ \_ \_ \_ BYTESTREAM**](mf-bytestream-last-modified-time-attribute.md) | Especifica cuándo se modificó por última vez una secuencia de bytes.                   |
| [**NOMBRE \_ DE ORIGEN DE MF \_ \_ BYTESTREAM**](mf-bytestream-origin-name-attribute.md)                | Especifica la dirección URL original de una secuencia de bytes.                     |



 

Los atributos siguientes se aplican a los controladores de flujo de bytes.



| Atributo                                                                                    | Descripción                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ ACEPTA ESCRITURA DE RECURSO \_ \_ COMPARTIDO](mf-bytestreamhandler-accepts-share-write.md) | Especifica si un controlador de flujo de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



