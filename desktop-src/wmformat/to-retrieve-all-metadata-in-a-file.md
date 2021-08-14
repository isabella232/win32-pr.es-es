---
title: Para recuperar todos los metadatos de un archivo
description: Para recuperar todos los metadatos de un archivo
ms.assetid: c1de58d7-25a8-4416-9ee9-6ebe641ed640
keywords:
- Windows SDK de formato multimedia, recuperación de metadatos
- Formato de sistemas avanzados (ASF), recuperación de metadatos
- ASF (formato de sistemas avanzados), recuperación de metadatos
- metadata,retrieving all
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fab81f151cbb661cc7769128e2d4371dd0b24869317d1888769ed66a60de86f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807475"
---
# <a name="to-retrieve-all-metadata-in-a-file"></a>Para recuperar todos los metadatos de un archivo

El ejemplo de código siguiente es una función que muestra todos los metadatos de un archivo. Para usar la función , debe pasar un puntero a la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) de un objeto del editor de metadatos, un objeto lector, un objeto de lector sincrónico o un objeto de escritor. También debe incluir el archivo de encabezado Stdio.h en algún lugar del proyecto. Para obtener más información sobre cómo usar este ejemplo, vea [Usar los ejemplos de código](using-the-code-examples.md).

Para mayor claridad, en este ejemplo no se muestran los valores de los atributos binarios y GUID. En el caso de los atributos binarios, debe comprobar si el nombre del atributo coincide con cualquiera de los atributos de metadatos complejos conocidos. Si es así, debe dar formato a la salida según la estructura usada para ese atributo. De forma similar, los valores de atributo GUID se pueden mostrar de varias maneras. Puede elegir mostrar cada miembro de la estructura de uno en uno o convertir la estructura en una cadena y mostrarla como un valor.


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

[**Recuperar atributos de metadatos**](retrieving-metadata-attributes.md)
</dt> </dl>

 

 




