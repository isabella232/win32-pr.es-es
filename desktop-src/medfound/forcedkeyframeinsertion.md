---
description: Inserción forzada de fotogramas clave
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserción forzada de fotogramas clave (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475839"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserción forzada de fotogramas clave (Microsoft Media Foundation)

Al configurar un objeto de codificador de vídeo, puede establecer un intervalo máximo para fotogramas clave en el contenido codificado. Sin embargo, el códec colocará fotogramas clave dentro de ese intervalo según lo dictado por el contenido; el intervalo de fotogramas clave no es constante. Para algunas aplicaciones, la distancia del fotograma clave es muy importante. Por ejemplo, una aplicación de edición de vídeo necesita fotogramas clave en ubicaciones que son lógicas para un editor, como en los saltos de escena y las transiciones de toma.

La inserción forzada de fotogramas clave es una característica que permite solicitar que un marco de entrada se codifica como un fotograma clave. El codificador intentará respetar estas solicitudes, pero la configuración del búfer (velocidad de bits y ventana de búfer) configurada para la sesión de codificación siempre tiene prioridad.

Los objetos del codificador de vídeo implementan la inserción forzada de fotogramas clave como respuesta a una extensión de unidad de datos asociada al ejemplo de entrada. Para obtener más información sobre las extensiones de unidad de datos, vea [Usar extensiones de unidad de datos](usingdataunitextensions.md).

Los datos de extensión para la inserción forzada de fotogramas clave se identifican mediante el siguiente valor GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Las extensiones individuales son **valores BOOL.** Establezca el valor en **TRUE para** indicar una solicitud de fotograma clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de extensiones de unidad de datos](usingdataunitextensions.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



