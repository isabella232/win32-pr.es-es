---
description: En este tema se proporciona información sobre cómo crear el objeto de indexador predeterminado proporcionado por Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Creación y configuración del indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061205"
---
# <a name="indexer-creation-and-configuration"></a>Creación y configuración del indexador

El *indexador* ASF es un componente de capa WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistemas avanzados (ASF). En este tema se proporciona información sobre cómo crear el objeto de indexador predeterminado proporcionado por Media Foundation.

Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

**Para crear e inicializar el indexador de ASF**

1.  Llame a [**la función MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para recibir un puntero [**MFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) al objeto indexador.
2.  Llame [**a IMFASFIndexer::SetFlags para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) especificar el modo de lectura o escritura para el objeto de indexador. De forma predeterminada, el indexador está configurado para la búsqueda hacia delante.

    

    | Usar                       | Marca                                           |
    |---------------------------|------------------------------------------------|
    | Lectura (búsqueda hacia delante) | Cero (valor predeterminado)                                 |
    | Lectura (búsqueda inversa) | **LECTURA DEL \_ INDEXADOR MFASF \_ PARA \_ \_ REVERSEPLAYBACK** |
    | Escritura                   | INDEXADOR MFASF \_ \_ ESCRIBE NUEVO \_ \_ ÍNDICE              |

    

     

    > [!Note]  
    > No se puede usar la misma instancia del indexador para lectura y escritura. Debe configurar el indexador para uno u otro.

     

3.  Llame [**a IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar el indexador especificando el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) del objeto ContentInfo que describe el archivo que se va a escribir o leer. El objeto ContentInfo contiene información que constituye el objeto [de encabezado asf](asf-file-structure.md). El objeto indexador requiere un objeto ContentInfo válido antes de generar o leer entradas de índice de un archivo ASF.

En el ejemplo de código siguiente se muestra cómo una aplicación puede crear e inicializar el objeto de indexador para trabajar con contenido de ASF específico. El objeto ContentInfo representa el objeto de encabezado ASF; el contenido se pasa como una secuencia de bytes.


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

[Indexador de ASF](asf-index-object.md)
</dt> <dt>

[Usar el indexador para buscar dentro de un archivo ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Usar el indexador para escribir un nuevo índice](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



