---
description: Uso de Windows multimedia con DirectShow Editing Services
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Uso de Windows multimedia con DirectShow Editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8c2e73fd4593a5f078c78e1e8290303b3574a314a504c4a555c46929361813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755935"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Uso de Windows multimedia con DirectShow Editing Services

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En esta sección se describe cómo usar Windows contenido basado en multimedia en una [aplicación DirectShow Editing Services](directshow-editing-services.md) (DES). Hay dos escenarios principales:

-   Clips de origen. Un proyecto DES puede contener clips de audio y vídeo de Windows archivos multimedia.
-   Formato de destino. Windows Los medios son un formato ideal para la salida final de un proyecto de edición de vídeo.

Para trabajar con Windows multimedia, la aplicación debe proporcionar un certificado de software, también denominado clave. Para ello, implementa un objeto de proveedor de claves. El proveedor de claves es un objeto COM que expone la **interfaz IServiceProvider.** Para obtener información sobre cómo implementar el proveedor de claves, vea [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

Para usar DES con Windows multimedia, los siguientes objetos DES requieren la clave de software:

-   El motor de representación, para la vista previa o la escritura de archivos.
-   El objeto MediaDet, para obtener fotogramas de vídeo o tipos multimedia de archivos ASF.
-   \[! Importante\]  
    > No use el motor de representación inteligente para leer o escribir archivos Windows multimedia. Use siempre el motor de representación básico (CLSID \_ RenderEngine).

     

Para proporcionar a un objeto la clave de software, consulte ese objeto para la interfaz **IObjectWithSite** y llame a **IObjectWithSite::SetSite** con un puntero al proveedor de claves. Por ejemplo, el código siguiente proporciona la clave de software al motor de representación:


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



Para usar Windows de origen multimedia en un proyecto DES, simplemente llame a **IObjectWithSite::SetSite** en el motor de representación con un puntero al proveedor de claves.

Para obtener información sobre cómo Windows archivos multimedia, vea Escribir un archivo multimedia Windows [en DES.](writing-a-windows-media-file-in-des.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 



