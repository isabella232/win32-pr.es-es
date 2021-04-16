---
description: Usar Windows Media con los servicios de edición de DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Usar Windows Media con los servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678621"
---
# <a name="using-windows-media-with-directshow-editing-services"></a>Usar Windows Media con los servicios de edición de DirectShow

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En esta sección se describe cómo usar el contenido basado en Windows Media en una aplicación de [servicios de edición de DirectShow](directshow-editing-services.md) (des). Hay dos escenarios principales:

-   Clips de origen. Un proyecto DES puede contener clips de audio y vídeo de archivos de Windows Media.
-   Formato de destino. Windows Media es un formato ideal para la salida final de un proyecto de edición de vídeo.

Para trabajar con archivos de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave. Para ello, implementa un objeto de proveedor de claves. El proveedor de claves es un objeto COM que expone la interfaz **IServiceProvider** . Para obtener información acerca de la implementación del proveedor de claves, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Para usar DES con archivos de Windows Media, los siguientes objetos DES requieren la clave de software:

-   El motor de representación, para la vista previa o la escritura de archivos.
-   El objeto MediaDet, para obtener fotogramas de vídeo o tipos de medios de archivos ASF.
-   \[! Aún\]  
    > No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media. Use siempre el motor de representación básico (CLSID \_ RenderEngine).

     

Para asignar a un objeto la clave de software, consulte ese objeto para la interfaz **IObjectWithSite** y llame a **IObjectWithSite:: SetSite** con un puntero al proveedor de claves. Por ejemplo, el código siguiente proporciona la clave de software al motor de representación:


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



Para usar clips de origen de Windows Media en un proyecto DES, basta con llamar a **IObjectWithSite:: SetSite** en el motor de representación con un puntero al proveedor de claves.

Para obtener información acerca de cómo escribir archivos de Windows Media, consulte [escribir un archivo de Windows Media en des](writing-a-windows-media-file-in-des.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



