---
title: Enumeración de receptores
description: Enumeración de receptores
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Formato de sistemas avanzados (ASF), enumeración de receptores
- ASF (formato de sistemas avanzados), enumeración de receptores
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- sinks,enumerating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029085"
---
# <a name="enumerating-sinks"></a>Enumeración de receptores

El escritor puede tener muchos receptores asociados. Puede enumerar los receptores que se han agregado al escritor mediante [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

El código de ejemplo de [obtención de mensajes de error de un receptor](getting-error-messages-from-a-sink.md) muestra la enumeración sink.

> [!Note]  
> Al enumerar los receptores, el receptor de archivo predeterminado creado en respuesta a una llamada a [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) se enumerará junto con cualquier otro receptor que haya agregado. Si solo usa el receptor de archivos predeterminado, puede acceder a él llamando a **GetSink** para el índice de receptor 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterAdvanced (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




