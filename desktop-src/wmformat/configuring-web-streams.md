---
title: Configuración de secuencias Web
description: Configuración de secuencias Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flujos, configurar secuencias Web
- códecs, configurar secuencias Web
- Flujos web, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357589"
---
# <a name="configuring-web-streams"></a>Configuración de secuencias Web

Las secuencias web son un tipo especializado de flujo de transferencia de archivos que se usa para proporcionar los archivos asociados a un sitio web en un único flujo. La configuración de la secuencia Web se resume en la tabla siguiente.



| Configuración                                            | Descripción                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **Tipo de medio de WM \_ \_ . majortype**                      | Establézcalo en WMMEDIATYPE \_ FileTransfer.                                                 |
| **Tipo de medio de WM \_ \_ . SubType**                        | Establezca en WMMEDIASUBTYPE \_ Webstream.                                                 |
| **Tipo de medio de WM \_ \_ . bFixedSizeSamples**              | Establézcalo en false.                                                                     |
| **Tipo de medio de WM \_ \_ . bTemporalCompression**           | Se establece en True.                                                                      |
| **Tipo de medio de WM \_ \_ . lSampleSize**                    | Establecer en 0.                                                                         |
| **Tipo de medio de WM \_ \_ . FormatType**                     | Establezca en WMFORMAT \_ Webstream.                                                       |
| **Tipo de medio de WM \_ \_ . pUnk**                           | Se establece en **null**.                                                                  |
| **Tipo de medio de WM \_ \_ . cbFormat**                       | Establézcalo en `sizeof(WMT_WEBSTREAM_FORMAT)`.                                            |
| **Tipo de medio de WM \_ \_ . pbFormat**                       | Se establece en la dirección de una estructura **de \_ \_ formato de Webstream WMT** configurada correctamente. |
| **\_Formato WEBstream de WMT \_ . cbSampleHeaderFixedData** | Establézcalo en `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.                                     |
| **\_Formato WEBstream de WMT \_ . wVersion**                | establézcalo en 1.                                                                         |
| **\_Formato WEBstream de WMT \_ . wreserved**               | Establecer en 0.                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Secuencias Web**](web-streams.md)
</dt> </dl>

 

 




