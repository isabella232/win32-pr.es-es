---
description: Especifica una lista de identificadores de idioma que especifica los idiomas contenidos en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de lista de idiomas, definido en la especificación ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: MF_PD_ASF_LANGLIST atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687970"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="deef2-104">MF \_ PD \_ ASF \_ atributo LANGLIST</span><span class="sxs-lookup"><span data-stu-id="deef2-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="deef2-105">Especifica una lista de identificadores de idioma que especifica los idiomas contenidos en un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="deef2-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="deef2-106">Este atributo corresponde al objeto de lista de idiomas, definido en la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="deef2-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="deef2-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="deef2-107">Data type</span></span>

<span data-ttu-id="deef2-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="deef2-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="deef2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="deef2-109">Remarks</span></span>

<span data-ttu-id="deef2-110">Este atributo se aplica a los descriptores de presentación para el contenido ASF.</span><span class="sxs-lookup"><span data-stu-id="deef2-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="deef2-111">El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del encabezado de objeto de lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="deef2-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="deef2-112">En la tabla siguiente se muestra el formato del BLOB:</span><span class="sxs-lookup"><span data-stu-id="deef2-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="deef2-113">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="deef2-113">Language List Object field</span></span> | <span data-ttu-id="deef2-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="deef2-114">Data type</span></span>    | <span data-ttu-id="deef2-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="deef2-115">Size</span></span>    | <span data-ttu-id="deef2-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="deef2-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="deef2-117">Recuento de registros de ID. de idioma</span><span class="sxs-lookup"><span data-stu-id="deef2-117">Language ID Records Count</span></span>  | <span data-ttu-id="deef2-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="deef2-118">**DWORD**</span></span>    | <span data-ttu-id="deef2-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="deef2-119">4 bytes</span></span> | <span data-ttu-id="deef2-120">Número de idiomas</span><span class="sxs-lookup"><span data-stu-id="deef2-120">Number of languages</span></span>                    |
| <span data-ttu-id="deef2-121">Registros de ID. de idioma</span><span class="sxs-lookup"><span data-stu-id="deef2-121">Language ID Records</span></span>        | <span data-ttu-id="deef2-122">**BYTES**\[\]</span><span class="sxs-lookup"><span data-stu-id="deef2-122">**BYTE**\[\]</span></span> | <span data-ttu-id="deef2-123">Varía</span><span class="sxs-lookup"><span data-stu-id="deef2-123">Varies</span></span>  | <span data-ttu-id="deef2-124">Matriz de cadenas de lenguaje (vea más abajo).</span><span class="sxs-lookup"><span data-stu-id="deef2-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="deef2-125">El primer **valor DWORD** es el número de idiomas seguido de una matriz de cadenas de identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="deef2-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="deef2-126">Cada cadena tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="deef2-126">Each string has the following format:</span></span>



| <span data-ttu-id="deef2-127">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="deef2-127">Language List Object field</span></span> | <span data-ttu-id="deef2-128">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="deef2-128">Data type</span></span>     | <span data-ttu-id="deef2-129">Tamaño</span><span class="sxs-lookup"><span data-stu-id="deef2-129">Size</span></span>    | <span data-ttu-id="deef2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="deef2-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="deef2-131">Longitud del identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="deef2-131">Language ID Length</span></span>         | <span data-ttu-id="deef2-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="deef2-132">**DWORD**</span></span>     | <span data-ttu-id="deef2-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="deef2-133">4 bytes</span></span> | <span data-ttu-id="deef2-134">Longitud de la cadena en bytes, incluido el tamaño del carácter **nulo** final.</span><span class="sxs-lookup"><span data-stu-id="deef2-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="deef2-135">Id. de idioma</span><span class="sxs-lookup"><span data-stu-id="deef2-135">Language ID</span></span>                | <span data-ttu-id="deef2-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="deef2-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="deef2-137">Varía</span><span class="sxs-lookup"><span data-stu-id="deef2-137">Varies</span></span>  | <span data-ttu-id="deef2-138">Una cadena terminada en null que contiene el nombre del idioma RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="deef2-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="deef2-139">Cada cadena es una etiqueta de lenguaje compatible con RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="deef2-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="deef2-140">Para obtener la etiqueta de idioma de una secuencia determinada en el archivo ASF, consulte en el descriptor de flujo el atributo [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Language \_ ID \_ index**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="deef2-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="deef2-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="deef2-141">Examples</span></span>

<span data-ttu-id="deef2-142">En el ejemplo siguiente se muestra cómo analizar la lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="deef2-142">The following example shows how to parse the language list.</span></span>


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a><span data-ttu-id="deef2-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deef2-143">Requirements</span></span>



| <span data-ttu-id="deef2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="deef2-144">Requirement</span></span> | <span data-ttu-id="deef2-145">Value</span><span class="sxs-lookup"><span data-stu-id="deef2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="deef2-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deef2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="deef2-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="deef2-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="deef2-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deef2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="deef2-149">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="deef2-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="deef2-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deef2-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="deef2-151"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="deef2-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deef2-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="deef2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deef2-153">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="deef2-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="deef2-154">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="deef2-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="deef2-155">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="deef2-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="deef2-156">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="deef2-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="deef2-157">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="deef2-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="deef2-158">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="deef2-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="deef2-159">Objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="deef2-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="deef2-160">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="deef2-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




