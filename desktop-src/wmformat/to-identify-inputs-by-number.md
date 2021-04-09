---
title: Para identificar entradas por número
description: Para identificar entradas por número
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF), identificación de entradas por número
- ASF (formato de sistemas avanzados), identificar entradas por número
- perfiles, identificación de entradas por número
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077305"
---
# <a name="to-identify-inputs-by-number"></a>Para identificar entradas por número

Cada muestra que se pasa al escritor debe estar asociada a un número de entrada. Cada número de entrada corresponde a una o más secuencias en el perfil que utiliza el escritor para escribir el archivo. En un perfil, los orígenes multimedia se identifican mediante un nombre de conexión. El escritor asocia un número de entrada con cada nombre de conexión cuando se establece el perfil para el escritor. Antes de poder pasar ejemplos al escritor, debe determinar qué datos esperan cada entrada. No se puede suponer que las entradas estarán en el mismo orden que los flujos de un perfil, aunque este sea el caso a menudo. Por lo tanto, la única manera confiable de hacer coincidir las entradas con secuencias es comparar el nombre de conexión de la entrada con el nombre de conexión de la secuencia.

Para identificar los nombres de conexión y los números de entrada correspondientes para un perfil cargado, realice los pasos siguientes:

1.  Cree un objeto de escritor y establezca un perfil para usarlo. Para obtener más información sobre la configuración de perfiles en el escritor, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md). Debe conocer los nombres de conexión que se usan para las secuencias en el perfil. Puede obtener el nombre de conexión desde dentro del perfil obteniendo el objeto de configuración de secuencia para cada flujo y llamando a [**IWMStreamConfig:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Para obtener más información sobre los perfiles y los objetos de configuración de secuencias, vea [trabajar con perfiles](working-with-profiles.md).
2.  Recupere el número total de entradas mediante una llamada a [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Recorra en bucle todas las entradas y realice los pasos siguientes para cada una de ellas.
    -   Recupere la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada mediante una llamada a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Recupere el nombre de conexión que corresponde al número de entrada mediante una llamada a [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). Una vez que tenga el nombre de la conexión, conocerá los flujos que están asociados a los números de entrada asignados por el escritor.

En el ejemplo de código siguiente se muestra el nombre de la conexión para cada entrada. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




