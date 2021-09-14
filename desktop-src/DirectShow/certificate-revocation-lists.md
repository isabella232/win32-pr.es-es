---
description: Listas de revocación de certificados
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listas de revocación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266607"
---
# <a name="certificate-revocation-lists"></a>Listas de revocación de certificados

En este tema se describe cómo examinar la lista de revocación de certificados (CRL) para los controladores revocados cuando se usa el Protocolo de protección de salida certificado (COPP).

La CRL contiene resúmenes de certificados revocados y solo Microsoft puede proporcionar y firmar. La CRL se distribuye a través de licencias de administración de derechos digitales (DRM). La CRL puede revocar cualquier certificado en la cadena de certificados del controlador. Si se revoca cualquier certificado de la cadena, también se revocan ese certificado y todos los certificados que se encuentran debajo de él en la cadena.

Para obtener la CRL, la aplicación debe usar el SDK de formato multimedia de Windows, versión 9 o posterior, y realizar los pasos siguientes:

1.  Llame **a WMCreateReader** para crear el objeto Windows lector del SDK de formato multimedia.
2.  Consulte el objeto reader para la **interfaz IWMDRMReader.**
3.  Llame **a IWMDRMReader::GetDRMProperty** con un valor de g \_ wszWMDRMNet Revocation para \_ obtener la CRL. Debe llamar a este método dos veces: una vez para obtener el tamaño del búfer que se va a asignar y otra para rellenar el búfer. La segunda llamada devuelve una cadena que contiene la CRL. Toda la cadena está codificada en base 64.
4.  Descodificar la cadena codificada en base 64. Para ello, puede usar la función **CryptStringToBinary.** Esta función forma parte de CryptoAPI.

> [!Note]  
> Para usar la **interfaz IWMDRMReader,** debe obtener una biblioteca DRM estática de Microsoft y vincular la aplicación a este archivo de biblioteca. Para obtener más información, vea el tema "Obtención de la biblioteca DRM necesaria" en la documentación Windows SDK de formato multimedia.

 

Si la CRL no está presente en el equipo del usuario, el **método GetDRMProperty** devuelve NS \_ E DRM \_ \_ UNSUPPORTED \_ PROPERTY. Actualmente, la única manera de obtener la CRL es adquirir una licencia DRM.

El código siguiente muestra una función que devuelve la CRL:


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



A continuación, la aplicación debe comprobar que la CRL es válida. Para ello, compruebe que el certificado CRL, que forma parte de la CRL, está firmado directamente por el certificado raíz de Microsoft y tiene el valor del elemento SignCRL establecido en 1. Compruebe también la firma de la CRL.

Una vez comprobada la CRL, la aplicación puede almacenarla. También se debe comprobar el número de versión de CRL antes de almacenarlo para que la aplicación siempre almacene la versión más reciente.

La CRL tiene el formato siguiente.



| Sección            | Contenido                                                             |
|--------------------|----------------------------------------------------------------------|
| Encabezado             | Número de entradas de 32 bits de crl versión 32 bits                           |
| Entradas de revocación | Varias entradas de revocación de 160 bits                                  |
| Certificado        | Longitud del certificado de 32 bits Certificado de longitud variable                 |
| Firma          | 8 bits signature type16-bit signature lengthVariable-length signature |



 

> [!Note]  
> Todos los valores enteros no tienen signo y se representan en la notación big-endian (orden de bytes de red).

 

Descripciones de la sección CRL

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Rúbrica
</dt> <dd>

El encabezado contiene el número de versión de la CRL y el número de entradas de revocación en la CRL. Una CRL puede contener cero o más entradas.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entradas de revocación
</dt> <dd>

Cada entrada de revocación es la síntesis de 160 bits de un certificado revocado. Compare este resumen con el elemento DigestValue dentro del certificado.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificado
</dt> <dd>

La sección de certificado contiene un valor de 32 bits que indica la longitud (en bytes) del certificado XML y su cadena de certificados, junto con una matriz de bytes que contiene el certificado XML de la entidad de certificación (CA) y la cadena de certificados que tiene Microsoft como raíz. El certificado debe estar firmado por una entidad de certificación que tenga la autoridad para emitir CRL.

> [!Note]  
> El certificado no debe terminar en null.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma
</dt> <dd>

La sección de firma contiene el tipo y la longitud de la firma, y la propia firma digital. El tipo de 8 bits se establece en 2 para indicar que usa SHA-1 con cifrado RSA de 1024 bits. La longitud es un valor de 16 bits que contiene la longitud de la firma digital en bytes. La firma digital se calcula en todas las secciones anteriores de la CRL.

La firma se calcula mediante el esquema de firma digital RSASSA-PSS que se define en PKCS \# 1 (versión 2.1). La función hash es SHA-1, que se define en Estándar federal de procesamiento de información (FIPS) 180-2, y la función de generación de máscaras es MGF1, que se define en la sección B.2.1 en PKCS \# 1 (versión 2.1). Las operaciones RSASP1 y RSAVP1 usan RSA con un módulo de 1024 bits con un exponente de verificación de 65537.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de salida certificado (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



