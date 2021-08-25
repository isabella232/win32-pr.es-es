---
title: Enumerar archivos en un trabajo
description: Para enumerar los archivos de un trabajo, llame al método IBackgroundCopyJob EnumFiles. El método devuelve un puntero de interfaz IEnumBackgroundCopyFiles que se usa para enumerar los archivos.
ms.assetid: 0e1fa024-4576-434c-bc5f-518d246b5faa
keywords:
- bits de trabajo de transferencia, enumeración de archivos
- enumerar bits de archivos
- enumerar BITS , archivos
- BITS de transferencia de archivos, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a986b8a8869008db34e97c1cc7e0cd733c301f5cdc57ce4ef6e313ff382479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801465"
---
# <a name="enumerating-files-in-a-job"></a>Enumerar archivos en un trabajo

Para enumerar los archivos de un trabajo, llame al [**método IBackgroundCopyJob::EnumFiles.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) El método devuelve un [**puntero de interfaz IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) que se usa para enumerar los archivos.

Tenga en cuenta que la lista enumerada es una instantánea de los archivos del trabajo en el momento en que se llama al método [**EnumFiles.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) Sin embargo, los valores de propiedad de esos objetos de archivo reflejan los valores actuales del archivo.

En el ejemplo siguiente se muestra cómo enumerar los archivos de un trabajo y recuperar sus propiedades. En el ejemplo se da por supuesto que el puntero de interfaz [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) es válido.


```C++
HRESULT hr = 0;
IBackgroundCopyJob* pJob;
IEnumBackgroundCopyFiles* pFiles = NULL;
IBackgroundCopyFile* pFile = NULL;
IBackgroundCopyFile3* pFile3 = NULL;
WCHAR* pLocalFileName = NULL;
ULONG cFileCount = 0;
ULONG idx = 0;

hr = pJob->EnumFiles(&pFiles);
if (SUCCEEDED(hr))
{
  //Get the count of files in the job. 
  pFiles->GetCount(&cFileCount);

  //Enumerate the files in the job.
  for (idx=0; idx<cFileCount; idx++)
  {
    hr = pFiles->Next(1, &pFile, NULL);
    if (S_OK == hr)
    {
      // Query for the latest file interface.
      hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
      pFile->Release();
      if (FAILED(hr))
      {
        wprintf(L"pFile->QueryInterface failed with 0x%x.\n", hr);
        goto cleanup;
      }

      // You can use the interface to retrieve the local and remote file
      // names, get the ranges to download if only part of the file content
      // is requested, determine the progress of the transfer, change the remote file
      // name, get the name of the temporary file that BITS uses to download
      // the file, determine if the file is downloaded from a peer, and set
      // the validation state of the file so it can be shared with peers.

      //Get the local name of the file.
      hr = pFile3->GetLocalName(&pLocalFileName);
      if (SUCCEEDED(hr))
      {
        //Do something with the file information.
      }

      CoTaskMemFree(pLocalFileName); 
      pFile3->Release();
      pFile3 = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pFiles->Release();
  pFiles = NULL;
}
```



 

 




