---
title: Configuración de web Secuencias
description: Configuración de web Secuencias
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- streams,configuring Web streams
- codecs,configuring Web streams
- Flujos web, configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251504"
---
# <a name="configuring-web-streams"></a>Configuración de web Secuencias

Las secuencias web son un tipo especializado de flujo de transferencia de archivos que se usa para entregar los archivos asociados a un sitio web en una sola secuencia. La configuración del flujo web se resume en la tabla siguiente.



| Parámetro                                            | Descripción                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                      | Se establece en WMMEDIATYPE \_ FileTransfer.                                                 |
| **WM \_ MEDIA \_ TYPE.subtype**                        | Establezca en WMMEDIASUBTYPE \_ WebStream.                                                 |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**              | Establezca en False.                                                                     |
| **WM \_ MEDIA \_ TYPE.bMentalCompression**           | Se establece en True.                                                                      |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                    | Establecer en 0.                                                                         |
| **WM \_ MEDIA \_ TYPE.formattype**                     | Establezca en WMFORMAT \_ WebStream.                                                       |
| **WM \_ MEDIA \_ TYPE.pUnk**                           | Se establece en **NULL.**                                                                  |
| **WM \_ MEDIA \_ TYPE.cbFormat**                       | Establézcalo en `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **WM \_ MEDIA \_ TYPE.pbFormat**                       | Establezca en la dirección de una estructura **DE FORMATO DE WMT \_ WEBSTREAM configurada \_ correctamente.** |
| **WMT \_ WEBSTREAM \_ FORMAT.cbSampleHeaderFixedData** | Establézcalo en `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **WMT \_ WEBSTREAM \_ FORMAT.wVersion**                | establézcalo en 1.                                                                         |
| **WMT \_ WEBSTREAM \_ FORMAT.wreserved**               | Establecer en 0.                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Web Secuencias**](web-streams.md)
</dt> </dl>

 

 




