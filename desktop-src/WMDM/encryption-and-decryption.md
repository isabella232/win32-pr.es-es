---
title: Cifrado y descifrado
description: Cifrado y descifrado
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Media Administrador de dispositivos, cifrado
- Administrador de dispositivos, cifrado
- aplicaciones de escritorio, cifrado
- proveedores de servicios, cifrado
- Guía de programación, cifrado
- cifrar
- Administrador de dispositivos de Windows Media, descifrado
- Administrador de dispositivos, descifrado
- aplicaciones de escritorio, descifrado
- proveedores de servicios, descifrado
- Guía de programación, descifrado
- descifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421312"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="37d7c-115">Cifrado y descifrado</span><span class="sxs-lookup"><span data-stu-id="37d7c-115">Encryption and Decryption</span></span>

<span data-ttu-id="37d7c-116">Windows Media Administrador de dispositivos requiere el cifrado de archivos enviados entre el proveedor de servicios y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37d7c-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="37d7c-117">Esto se puede hacer de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="37d7c-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="37d7c-118">Si el proveedor de servicios solo admite [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) y [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), la aplicación y el proveedor de servicios deben cifrar y descifrar los datos mediante los métodos [CSecureChannelClient](csecurechannelclient-class.md) y [CSecureChannelServer](csecurechannelserver-class.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="37d7c-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="37d7c-119">Si el proveedor de servicios admite [**IMDSPObject2:: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) y [**IMDSPObject2:: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), la aplicación puede evitar la costosa autenticación de mensajes de canal seguro.</span><span class="sxs-lookup"><span data-stu-id="37d7c-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="37d7c-120">(El canal seguro se conserva para que los proveedores de servicios heredados que no implementan [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) sigan funcionando).</span><span class="sxs-lookup"><span data-stu-id="37d7c-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="37d7c-121">El requisito de cifrado evita que aplicaciones malintencionadas obtengan los datos que se pasan entre los componentes de software y también protege la integridad de los datos que se envían al dispositivo o desde él.</span><span class="sxs-lookup"><span data-stu-id="37d7c-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="37d7c-122">Los tres métodos siguientes requieren cifrado o descifrado.</span><span class="sxs-lookup"><span data-stu-id="37d7c-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="37d7c-123">Método</span><span class="sxs-lookup"><span data-stu-id="37d7c-123">Method</span></span>                                                                          | <span data-ttu-id="37d7c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="37d7c-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37d7c-125">**IWMDMOperation::TransferObjectData**</span><span class="sxs-lookup"><span data-stu-id="37d7c-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="37d7c-126">Aplicación Cifrado o descifrado, en función de si la aplicación envía o recibe datos.</span><span class="sxs-lookup"><span data-stu-id="37d7c-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="37d7c-127">**IMDSPObject:: Read**</span><span class="sxs-lookup"><span data-stu-id="37d7c-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="37d7c-128">(Proveedor de servicios) Cifra.</span><span class="sxs-lookup"><span data-stu-id="37d7c-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="37d7c-129">**IMDSPObject:: Write**</span><span class="sxs-lookup"><span data-stu-id="37d7c-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="37d7c-130">(Proveedor de servicios) Descifrado.</span><span class="sxs-lookup"><span data-stu-id="37d7c-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="37d7c-131">El cifrado y descifrado se realizan mediante llamadas a un solo método.</span><span class="sxs-lookup"><span data-stu-id="37d7c-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="37d7c-132">[**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)) para las aplicaciones o [**CSecureChannelServer:: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) para los proveedores de servicios realiza el cifrado.</span><span class="sxs-lookup"><span data-stu-id="37d7c-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="37d7c-133">El descifrado se realiza mediante [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) for Applications o [**CSecureChannelServer::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) para proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="37d7c-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="37d7c-134">Los parámetros son idénticos entre los métodos de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="37d7c-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="37d7c-135">En los pasos siguientes se muestra cómo cifrar y descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="37d7c-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="37d7c-136">(Estos pasos solo son importantes si la aplicación se comunica con un proveedor de servicios heredado que no implementa [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)).</span><span class="sxs-lookup"><span data-stu-id="37d7c-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="37d7c-137">**Cifrado**</span><span class="sxs-lookup"><span data-stu-id="37d7c-137">**Encryption**</span></span>

1.  <span data-ttu-id="37d7c-138">Cree la clave MAC para los datos cifrados, como se describe en [Message Authentication](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="37d7c-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="37d7c-139">Llame a **EncryptParam** con los datos que se van a cifrar para realizar el cifrado en contexto.</span><span class="sxs-lookup"><span data-stu-id="37d7c-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="37d7c-140">En el ejemplo de código siguiente se muestra la implementación de un proveedor de servicios de [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span><span class="sxs-lookup"><span data-stu-id="37d7c-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="37d7c-141">Este método crea la clave MAC con los datos para cifrar y el tamaño de los datos y los envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37d7c-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="37d7c-142">**Descifrado**</span><span class="sxs-lookup"><span data-stu-id="37d7c-142">**Decryption**</span></span>

1.  <span data-ttu-id="37d7c-143">Llame a **DecryptParam** con los datos que se van a cifrar para realizar el descifrado en contexto.</span><span class="sxs-lookup"><span data-stu-id="37d7c-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="37d7c-144">Compruebe la clave MAC de los datos descifrados, tal como se describe en [Message Authentication](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="37d7c-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="37d7c-145">En el ejemplo de código siguiente se muestra la implementación de un proveedor de servicios de [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span><span class="sxs-lookup"><span data-stu-id="37d7c-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="37d7c-146">Este método crea la clave MAC con los datos para cifrar y el tamaño de los datos y los envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="37d7c-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="37d7c-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37d7c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37d7c-148">**Usar canales autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="37d7c-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 