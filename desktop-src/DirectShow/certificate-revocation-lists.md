---
description: Listas de revocación de certificados
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listas de revocación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666117"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="9b9ca-103">Listas de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="9b9ca-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="9b9ca-104">En este tema se describe cómo examinar la lista de revocación de certificados (CRL) para los controladores revocados cuando se usa el protocolo de protección de la salida certificada (COPP).</span><span class="sxs-lookup"><span data-stu-id="9b9ca-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="9b9ca-105">La CRL contiene resúmenes de los certificados revocados y solo Microsoft puede proporcionarlos y firmarlos.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="9b9ca-106">La CRL se distribuye a través de licencias de administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="9b9ca-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="9b9ca-107">La CRL puede revocar cualquier certificado de la cadena de certificados del controlador.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="9b9ca-108">Si se revoca algún certificado de la cadena, el certificado y todos los certificados que se encuentran por debajo en la cadena también se revocan.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="9b9ca-109">Para obtener la CRL, la aplicación debe usar Windows Media Format SDK, versión 9 o posterior, y realizar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b9ca-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="9b9ca-110">Llame a **WMCreateReader** para crear el objeto lector del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="9b9ca-111">Consulte el objeto de lector para la interfaz **IWMDRMReader** .</span><span class="sxs-lookup"><span data-stu-id="9b9ca-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="9b9ca-112">Llame a **IWMDRMReader:: GetDRMProperty** con un valor de g \_ wszWMDRMNet \_ revocación para obtener la CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="9b9ca-113">Debe llamar a este método dos veces: una vez para obtener el tamaño del búfer que se va a asignar y para rellenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="9b9ca-114">La segunda llamada devuelve una cadena que contiene la CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="9b9ca-115">Toda la cadena es la codificación base-64.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="9b9ca-116">Descodifique la cadena codificada en base 64.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="9b9ca-117">Para ello, puede usar la función **CryptStringToBinary** .</span><span class="sxs-lookup"><span data-stu-id="9b9ca-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="9b9ca-118">Esta función forma parte de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="9b9ca-119">Para usar la interfaz **IWMDRMReader** , debe obtener una biblioteca DRM estática de Microsoft y vincular la aplicación a este archivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="9b9ca-120">Para obtener más información, vea el tema "obtención de la biblioteca DRM necesaria" en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="9b9ca-121">Si la CRL no está presente en el equipo del usuario, el método **GetDRMProperty** devuelve la \_ \_ \_ propiedad no compatible con DRM de NS E \_ .</span><span class="sxs-lookup"><span data-stu-id="9b9ca-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="9b9ca-122">Actualmente, la única manera de obtener la CRL es adquirir una licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="9b9ca-123">En el código siguiente se muestra una función que devuelve la CRL:</span><span class="sxs-lookup"><span data-stu-id="9b9ca-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="9b9ca-124">A continuación, la aplicación debe comprobar que la CRL es válida.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="9b9ca-125">Para ello, compruebe que el certificado de CRL, que forma parte de la CRL, está firmado directamente por el certificado raíz de Microsoft y tiene el valor del elemento SignCRL establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="9b9ca-126">Además, Compruebe la firma de la CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="9b9ca-127">Una vez comprobada la CRL, la aplicación puede almacenarla.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="9b9ca-128">El número de versión de CRL también debe comprobarse antes de almacenar para que la aplicación Almacene siempre la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="9b9ca-129">La CRL tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-129">The CRL has the following format.</span></span>



| <span data-ttu-id="9b9ca-130">Sección</span><span class="sxs-lookup"><span data-stu-id="9b9ca-130">Section</span></span>            | <span data-ttu-id="9b9ca-131">Contenido</span><span class="sxs-lookup"><span data-stu-id="9b9ca-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="9b9ca-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b9ca-132">Header</span></span>             | <span data-ttu-id="9b9ca-133">32 de CRL de bits version32 bits número de entradas</span><span class="sxs-lookup"><span data-stu-id="9b9ca-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="9b9ca-134">Entradas de revocación</span><span class="sxs-lookup"><span data-stu-id="9b9ca-134">Revocation Entries</span></span> | <span data-ttu-id="9b9ca-135">Varias entradas de revocación de 160 bits</span><span class="sxs-lookup"><span data-stu-id="9b9ca-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="9b9ca-136">Certificado</span><span class="sxs-lookup"><span data-stu-id="9b9ca-136">Certificate</span></span>        | <span data-ttu-id="9b9ca-137">certificado de 32 bits lengthVariable-length</span><span class="sxs-lookup"><span data-stu-id="9b9ca-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="9b9ca-138">Firma</span><span class="sxs-lookup"><span data-stu-id="9b9ca-138">Signature</span></span>          | <span data-ttu-id="9b9ca-139">firma de 8 bits type16 de bits lengthVariable-signatura de longitud</span><span class="sxs-lookup"><span data-stu-id="9b9ca-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="9b9ca-140">Todos los valores enteros están sin signo y se representan en notación Big-Endian (orden de bytes de red).</span><span class="sxs-lookup"><span data-stu-id="9b9ca-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="9b9ca-141">Descripciones de la sección CRL</span><span class="sxs-lookup"><span data-stu-id="9b9ca-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="9b9ca-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b9ca-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="9b9ca-143">El encabezado contiene el número de versión de la CRL y el número de entradas de revocación de la CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="9b9ca-144">Una CRL puede contener cero o más entradas.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="9b9ca-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entradas de revocación</span><span class="sxs-lookup"><span data-stu-id="9b9ca-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="9b9ca-146">Cada entrada de revocación es el Resumen de 160 bits de un certificado revocado.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="9b9ca-147">Compare esta síntesis con el elemento DigestValue en el certificado.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="9b9ca-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificado</span><span class="sxs-lookup"><span data-stu-id="9b9ca-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="9b9ca-149">La sección de certificado contiene un valor de 32 bits que indica la longitud (en bytes) del certificado XML y su cadena de certificados, junto con una matriz de bytes que contiene el certificado XML de la entidad de certificación (CA) y la cadena de certificados que tiene Microsoft como raíz.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="9b9ca-150">El certificado debe estar firmado por una entidad de certificación (CA) que tenga autoridad para emitir CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="9b9ca-151">El certificado no debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="9b9ca-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatura</span><span class="sxs-lookup"><span data-stu-id="9b9ca-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="9b9ca-153">La sección Signature contiene el tipo y la longitud de la firma, y la propia firma digital.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="9b9ca-154">El tipo de 8 bits se establece en 2 para indicar que usa SHA-1 con cifrado RSA de 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="9b9ca-155">La longitud es un valor de 16 bits que contiene la longitud de la firma digital en bytes.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="9b9ca-156">La firma digital se calcula en todas las secciones anteriores de la CRL.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="9b9ca-157">La firma se calcula mediante el esquema de firma digital RSASSA-PSS que se define en PKCS \# 1 (versión 2,1).</span><span class="sxs-lookup"><span data-stu-id="9b9ca-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="9b9ca-158">La función hash es SHA-1, que se define en Estándar federal de procesamiento de información (FIPS) 180-2 y la función de generación de máscara es MGF1, que se define en la sección B. 2.1 en PKCS \# 1 (versión 2,1).</span><span class="sxs-lookup"><span data-stu-id="9b9ca-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="9b9ca-159">Las operaciones RSASP1 y RSAVP1 usan RSA con un módulo de 1024 bits con un exponente de comprobación de 65537.</span><span class="sxs-lookup"><span data-stu-id="9b9ca-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9b9ca-160">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b9ca-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b9ca-161">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="9b9ca-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



