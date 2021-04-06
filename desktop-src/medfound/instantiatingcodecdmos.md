---
description: Crear instancias del códec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Crear instancias del códec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001118"
---
# <a name="instantiating-codec-dmos"></a>Crear instancias del códec DMOs

Puede crear un códec DMO mediante una llamada a la función com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Debe pasar el identificador de clase de DMO, el identificador de interfaz de **IMediaObject** y un puntero a un puntero **IMediaObject** .

Los identificadores de clase del códec DMOs se definen como constantes en el archivo de encabezado wmcodecdsp. h.

La constante para el identificador de la interfaz **IMediaObject** es IID \_ IMediaObject.

En el ejemplo de código siguiente se muestra cómo crear una instancia de un códec DMO:


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
