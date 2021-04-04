---
description: En este tema se proporciona información sobre cómo crear el objeto indexador predeterminado proporcionado por Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Creación y configuración de indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277841"
---
# <a name="indexer-creation-and-configuration"></a>Creación y configuración de indexador

El *indexador* ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF). En este tema se proporciona información sobre cómo crear el objeto indexador predeterminado proporcionado por Media Foundation.

Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).

**Para crear e inicializar el indizador ASF**

1.  Llame a la función [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para recibir un puntero [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) al objeto indexador.
2.  Llame a [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) para especificar el modo de lectura o escritura para el objeto indexador. De forma predeterminada, el indexador está configurado para búsquedas hacia delante.

    

    | Use                       | Marca                                           |
    |---------------------------|------------------------------------------------|
    | Lectura (búsquedas hacia delante) | Cero (valor predeterminado)                                 |
    | Lectura (búsqueda inversa) | **\_indexador \_ de MFASF leído \_ para \_ REVERSEPLAYBACK** |
    | Escritura                   | Índice nuevo de MFASF de \_ escritura de indexador \_ \_ \_              |

    

     

    > [!Note]  
    > No se puede usar la misma instancia del indexador para lectura y escritura. Debe configurar el indizador para uno u otro.

     

3.  Llame a [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar el indizador especificando el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del objeto ContentInfo que describe el archivo que se va a escribir o leer. El objeto ContentInfo contiene información que constituye el [objeto de encabezado ASF](asf-file-structure.md). El objeto de indexador requiere un objeto ContentInfo válido antes de generar o leer entradas de índice de un archivo ASF.

En el ejemplo de código siguiente se muestra cómo una aplicación puede crear e inicializar el objeto de indexador para trabajar con contenido ASF específico. El objeto ContentInfo representa el objeto de encabezado ASF; el contenido se pasa como un flujo de bytes.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Indexador ASF](asf-index-object.md)
</dt> <dt>

[Uso del indexador para buscar en un archivo ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Usar el indexador para escribir un nuevo índice](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



