---
title: Para recuperar todos los metadatos de un archivo
description: Para recuperar todos los metadatos de un archivo
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- SDK de Windows Media Format, recuperar metadatos
- Advanced Systems Format (ASF), recuperar metadatos
- ASF (formato de sistemas avanzados), recuperar metadatos
- metadatos, recuperar todos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc5d63a27cd4455d8d39cebee894dfbfc8d5bf2c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105676341"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>Para recuperar todos los metadatos de un archivo

El siguiente ejemplo de código es una función que muestra todos los metadatos de un archivo. Para usar la función, debe pasar un puntero a la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) de un objeto de editor de metadatos, un objeto de lector, un objeto de lector sincrónico o un objeto de escritor. También debe incluir el archivo de encabezado stdio. h en algún lugar del proyecto. Para obtener más información sobre cómo usar este ejemplo, vea [usar los ejemplos de código](using-the-code-examples.md).

Para mayor claridad, en este ejemplo no se muestran los valores de los atributos binarios y GUID. En el caso de los atributos binarios, debe comprobar si el nombre del atributo coincide con alguno de los atributos de metadatos complejos conocidos. Si lo hace, debe dar formato a la salida según la estructura utilizada para ese atributo. Del mismo modo, los valores de atributo GUID se pueden mostrar de varias maneras. Puede optar por mostrar cada miembro de la estructura de una en una o convertir la estructura en una cadena y mostrarla como un valor.


```C++
HRESULT ShowAllAttributes(IWMHeaderInfo3* pHeaderInfo)
{
    HRESULT hr          = S_OK;
    
    WORD    cAttributes = 0;
    WCHAR*  pwszName    = NULL;
    WORD    cchName     = 0;
    BYTE*   pbValue     = NULL;
    DWORD   cbValue     = 0;
    WORD    langIndex   = 0;
    WORD    attIndex    = 0;

    WMT_ATTR_DATATYPE attType;

    // Get the total number of attributes in the file.

    hr = pHeaderInfo->GetAttributeCountEx(0xFFFF, &cAttributes);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all the attributes, retrieving and displaying each.

    for(attIndex = 0; attIndex < cAttributes; attIndex++)
    {
        // Get the required buffer lengths for the name and value.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                NULL,
                                                &cchName,
                                                NULL,
                                                NULL,
                                                NULL,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Allocate the buffers.

        pwszName = new WCHAR[cchName];
        if(pwszName == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        pbValue = new BYTE[cbValue];
        if(pbValue == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }

        // Get the attribute.

        hr = pHeaderInfo->GetAttributeByIndexEx(0xFFFF,
                                                attIndex,
                                                pwszName,
                                                &cchName,
                                                &attType,
                                                &langIndex,
                                                pbValue,
                                                &cbValue);
        GOTO_EXIT_IF_FAILED(hr);

        // Display the attribute global index and name.

        printf("%3d - %S (Language %d):\n\t ", attIndex, pwszName, langIndex);

        // Display the attribute depending upon type.

        switch(attType)
        {
        case WMT_TYPE_DWORD:
        case WMT_TYPE_QWORD:
        case WMT_TYPE_WORD:
            printf("%d\n\n", (DWORD) *pbValue);
            break;
        case WMT_TYPE_STRING:
            printf("%S\n\n", (WCHAR*) pbValue);
            break;
        case WMT_TYPE_BINARY:
            printf("<binary value>\n\n");
            break;
        case WMT_TYPE_BOOL:
            printf("%s\n\n", ((BOOL) *pbValue == TRUE) ? "True" : "False");
            break;
        case WMT_TYPE_GUID:
            printf("<GUID value>\n\n", (DWORD) *pbValue);
            break;
        }

        // Release allocated memory for the next pass.

        SAFE_ARRAY_DELETE(pwszName);
        SAFE_ARRAY_DELETE(pbValue);
        cchName = 0;
        cbValue = 0;
    } // End for attIndex.

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Recuperación de atributos de metadatos**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




