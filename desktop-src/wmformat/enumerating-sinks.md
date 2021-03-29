---
title: Enumerar receptores
description: Enumerar receptores
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), enumeración de receptores
- ASF (formato de sistemas avanzados), enumeración de receptores
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789171"
---
# <a name="enumerating-sinks"></a>Enumerar receptores

El escritor puede tener muchos receptores asociados. Puede enumerar los receptores que se han agregado al escritor mediante [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) y [**IWMWriterAdvanced:: GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

El código de ejemplo de la [sección obtención de mensajes de error de un receptor](getting-error-messages-from-a-sink.md) muestra la enumeración de receptores.

> [!Note]  
> Al enumerar los receptores, el receptor de archivos predeterminado creado en respuesta a una llamada a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) se enumerará junto con cualquier otro receptor que haya agregado. Si solo usa el receptor de archivos predeterminado, puede acceder a él mediante una llamada a **GetSink** para el índice de receptor 0.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




