---
title: Usar atributos de metadatos complejos
description: Usar atributos de metadatos complejos
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- SDK de Windows Media Format, atributos de metadatos complejos
- Advanced Systems Format (ASF), atributos de metadatos complejos
- ASF (formato de sistemas avanzados), atributos de metadatos complejos
- metadatos, atributos complejos
- atributos de metadatos complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd03c656a8cba5342d21e41932365455daa8bfa
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358688"
---
# <a name="using-complex-metadata-attributes"></a><span data-ttu-id="180c9-108">Usar atributos de metadatos complejos</span><span class="sxs-lookup"><span data-stu-id="180c9-108">Using Complex Metadata Attributes</span></span>

<span data-ttu-id="180c9-109">El SDK de Windows Media Format admite atributos de metadatos complejos, que son atributos que tienen valores representados por una estructura.</span><span class="sxs-lookup"><span data-stu-id="180c9-109">The Windows Media Format SDK supports complex metadata attributes, which are attributes that have values represented by a structure.</span></span> <span data-ttu-id="180c9-110">Dado que todos los atributos deben tener un tipo de datos definido en la enumeración de [**\_ \_ tipos**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) de datos de atributo WMT, todos los atributos de metadatos complejos se tratan como archivos **\_ \_ binarios de tipo WMT**.</span><span class="sxs-lookup"><span data-stu-id="180c9-110">Because all attributes must have a data type defined in the [**WMT\_ATTR\_DATATYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) enumeration, all complex metadata attributes are treated as **WMT\_TYPE\_BINARY**.</span></span> <span data-ttu-id="180c9-111">Al escribir un atributo complejo, convierta el puntero a la estructura como un puntero de byte.</span><span class="sxs-lookup"><span data-stu-id="180c9-111">When writing a complex attribute, cast the pointer to the structure as a byte pointer.</span></span> <span data-ttu-id="180c9-112">Al recuperar un atributo complejo, convierta la matriz de bytes establecida por [**IWMHeaderInfo3:: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) como la estructura adecuada.</span><span class="sxs-lookup"><span data-stu-id="180c9-112">When you retrieve a complex attribute, cast the array of bytes set by [**IWMHeaderInfo3::GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) as the appropriate structure.</span></span>

<span data-ttu-id="180c9-113">Los ejemplos de código siguientes muestran cómo establecer y recuperar un atributo de metadatos complejo.</span><span class="sxs-lookup"><span data-stu-id="180c9-113">The following code examples show how to set and retrieve a complex metadata attribute.</span></span> <span data-ttu-id="180c9-114">La primera función agrega un atributo de texto de usuario, la segunda función recupera uno.</span><span class="sxs-lookup"><span data-stu-id="180c9-114">The first function adds a user text attribute, the second function retrieves one.</span></span> <span data-ttu-id="180c9-115">Para obtener más información sobre cómo usar estos ejemplos, vea [usar los ejemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="180c9-115">For more information about how to use these examples, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="180c9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="180c9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="180c9-117">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="180c9-117">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




