---
description: Creación del objeto divisor de ASF
ms.assetid: 448e2b38-70f7-4491-aac8-ee988a6f7473
title: Creación del objeto divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42c8033a0861102f6d66b22e43516a616d6428b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263404"
---
# <a name="creating-the-asf-splitter-object"></a>Creación del objeto divisor de ASF

El objeto *divisor* ASF es un objeto de capa WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistemas avanzados (ASF). Para crear una nueva instancia del objeto divisor ASF, llame a la [**función MFCreateASFSplitter.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) Esta función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) que representa un objeto divisor vacío.

Para que el divisor pueda empezar a analizar, la aplicación debe inicializar el divisor con información del objeto de encabezado asf. Para inicializar el divisor, llame al [**método IMFASFSplitter::Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) Este método toma un puntero al objeto ContentInfo de [ASF](asf-contentinfo-object.md) que contiene información de encabezado del archivo ASF que se va a analizar. La aplicación debe inicializar el objeto ContentInfo antes de pasarlo al divisor para que la aplicación conozca las características del archivo multimedia. El método **Initialize** del divisor extrae información de secuencia del objeto ContentInfo, como los números de secuencia, para que el divisor pueda analizar los paquetes de datos.

### <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo crear un divisor e inicializar con un objeto ContentInfo existente.


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



> [!Note]  
> En este ejemplo se usa [la función SafeRelease para](saferelease.md) liberar punteros de interfaz.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> </dl>

 

 



