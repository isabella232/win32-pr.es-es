---
title: Para identificar entradas por número
description: Para identificar entradas por número
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Formato de sistemas avanzados (ASF), identificar entradas por número
- ASF (formato de sistemas avanzados), identificar entradas por número
- profiles,identifying inputs by number
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff09a81cac98edc6f14ded98ba9852501bfdfef4c5e40affa908c0ff710e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807535"
---
# <a name="to-identify-inputs-by-number"></a>Para identificar entradas por número

Cada ejemplo que pase al escritor debe estar asociado a un número de entrada. Cada número de entrada corresponde a una o varias secuencias del perfil que usa el escritor para escribir el archivo. En un perfil, los orígenes multimedia se identifican mediante un nombre de conexión. El escritor asocia un número de entrada a cada nombre de conexión cuando se establece el perfil para el escritor. Para poder pasar ejemplos al escritor, debe determinar qué datos espera cada entrada. No se puede suponer que las entradas estarán en el mismo orden que las secuencias de un perfil, aunque esto suele ser así. Por lo tanto, la única manera confiable de hacer coincidir entradas con secuencias es comparar el nombre de conexión de la entrada con el nombre de conexión de la secuencia.

Para identificar los nombres de conexión y los números de entrada correspondientes para un perfil cargado, realice los pasos siguientes:

1.  Cree un objeto de escritor y establezca un perfil que se usará. Para obtener más información sobre cómo establecer perfiles en el sistema de escritura, vea [Para usar perfiles con el escritor](to-use-profiles-with-the-writer.md). Debe conocer los nombres de conexión usados para las secuencias del perfil. Puede obtener el nombre de conexión desde dentro del perfil obteniendo el objeto de configuración de flujo para cada secuencia y llamando a [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname). Para obtener más información sobre los perfiles y los objetos de configuración de secuencias, vea [Trabajar con perfiles.](working-with-profiles.md)
2.  Recupere el número total de entradas llamando a [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).
3.  Recorrer en bucle todas las entradas y realizar los pasos siguientes para cada una de ellas.
    -   Recupere la [**interfaz IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada llamando a [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).
    -   Recupere el nombre de conexión que corresponde al número de entrada llamando a [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname). Una vez que tenga el nombre de conexión, conocerá las secuencias asociadas a los números de entrada asignados por el escritor.

En el código de ejemplo siguiente se muestra el nombre de conexión de cada entrada. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


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

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




