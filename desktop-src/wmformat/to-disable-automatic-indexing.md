---
title: Para deshabilitar la indexación automática
description: Para deshabilitar la indexación automática
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows SDK de formato multimedia, deshabilitar la indexación automática
- Windows SDK de formato multimedia, indexación automática
- Formato de sistemas avanzados (ASF), deshabilitar la indexación automática
- ASF (formato de sistemas avanzados), deshabilitar la indexación automática
- Formato de sistemas avanzados (ASF), indexación automática
- ASF (formato de sistemas avanzados), indexación automática
- índices, deshabilitar la indexación automática
- índices, indexación automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3b63d58b8f9a0fbbdff88369832b67abca7d9f11a39c56613c6e5d867d6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699917"
---
# <a name="to-disable-automatic-indexing"></a>Para deshabilitar la indexación automática

Es posible que no siempre quiera que se genere un índice de forma predeterminada al escribir un archivo ASF. Puede deshabilitar la indexación automática mediante el [**método IWMWriterFileSink3::SetAutoIndexing.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing)

En el código de ejemplo siguiente se muestra cómo deshabilitar la indexación automática por parte del escritor.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> </dl>

 

 




