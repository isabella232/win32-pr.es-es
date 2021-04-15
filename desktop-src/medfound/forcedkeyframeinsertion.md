---
description: Inserción de fotogramas clave forzada
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Inserción de fotogramas clave forzada (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496810"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Inserción de fotogramas clave forzada (Microsoft Media Foundation)

Al configurar un objeto de codificador de vídeo, puede establecer un intervalo máximo para los fotogramas clave en el contenido codificado. Sin embargo, el códec colocará fotogramas clave dentro de ese intervalo tal como lo indica el contenido; el intervalo de fotogramas clave no es constante. En algunas aplicaciones, la distancia del fotograma clave es muy importante. Por ejemplo, una aplicación de edición de vídeo necesita fotogramas clave en las ubicaciones que son lógicas para un editor, como en los saltos de escena y las transiciones de captura.

La inserción de fotogramas clave forzada es una característica que permite solicitar que un fotograma de entrada se codifique como un fotograma clave. El codificador tratará de cumplir estas solicitudes, pero la configuración de búfer (velocidad de bits y ventana de búfer) configurada para la sesión de codificación siempre tiene prioridad.

Los objetos del codificador de vídeo implementan la inserción del fotograma clave forzada como respuesta a una extensión de unidad de datos asociada a la muestra de entrada. Para obtener más información acerca de las extensiones de unidad de datos, consulte [uso de extensiones de unidad de datos](usingdataunitextensions.md).

Los datos de extensión para la inserción de fotogramas clave forzada se identifican mediante el siguiente valor de GUID: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Las extensiones individuales son valores **bool** . Establezca el valor en **true** para indicar una solicitud de fotograma clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de extensiones de unidad de datos](usingdataunitextensions.md)
</dt> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



