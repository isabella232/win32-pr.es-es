---
description: Creación de instancias de DDO de códec
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Creación de instancias de DDO de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957555"
---
# <a name="instantiating-codec-dmos"></a>Creación de instancias de DDO de códec

Puede crear un códec DMO mediante una llamada a la [**función COM CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) Debe pasar el identificador de clase del DMO, el identificador de interfaz de **IMediaObject** y un puntero a un **puntero IMediaObject.**

Los identificadores de clase de las DDO de códec se definen como constantes en el archivo de encabezado wmcodecdsp.h.

La constante para el **identificador de interfaz IMediaObject** es IID \_ IMediaObject.

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

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
