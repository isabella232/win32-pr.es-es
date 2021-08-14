---
title: Para detener la indexación en curso
description: Para detener la indexación en curso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows SDK de formato multimedia, detener la indexación en curso
- Formato de sistemas avanzados (ASF), detener la indexación en curso
- ASF (formato de sistemas avanzados), detener la indexación en curso
- índices, detener la indexación en curso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432628"
---
# <a name="to-stop-indexing-in-progress"></a>Para detener la indexación en curso

Después de comenzar la indexación con una llamada a [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), el indexador normalmente continuará hasta que se indexe el archivo. Puede detener las operaciones de indexación llamando al [**método IWMIndexer::Cancel.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) Después de cancelar la indexación, puede llamar de nuevo a **StartIndexing,** pero el indexador se iniciará desde el principio del archivo en lugar de reanudarse desde el punto de cancelación.

Dado **que StartIndexing** es una llamada asincrónica, normalmente deberá llamar a **Cancel** desde algún otro subproceso o controlador de eventos de la aplicación. Normalmente, **se** llamará a Cancel desde un procedimiento de evento asociado a un control de botón de Windows aplicación.

Cuando se cancela la indexación, el indexador pasará un mensaje de estado WMT CLOSED, igual que si el archivo se \_ hubiera indexado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMIndexer (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




