---
title: Cifrado y descifrado
description: Cifrado y descifrado
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Media Administrador de dispositivos,encryption
- Administrador de dispositivos,encryption
- aplicaciones de escritorio, cifrado
- proveedores de servicios, cifrado
- guía de programación, cifrado
- El cifrado
- Windows Media Administrador de dispositivos,decryption
- Administrador de dispositivos,decryption
- aplicaciones de escritorio, descifrado
- proveedores de servicios, descifrado
- guía de programación, descifrado
- descifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890329"
---
# <a name="encryption-and-decryption"></a>Cifrado y descifrado

Windows El Administrador de dispositivos requiere el cifrado de archivos enviados entre el proveedor de servicios y la aplicación. Esto se puede hacer de dos maneras:

-   Si el proveedor de servicios solo admite [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) e [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), la aplicación y el proveedor de servicios deben cifrar y descifrar los datos mediante los métodos [CSecureChannelClient](csecurechannelclient-class.md) y [CSecureChannelServer,](csecurechannelserver-class.md) respectivamente.
-   Si el proveedor de servicios admite [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) e [**IMDSPObject2::WriteOnClearChannel,**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel)la aplicación puede evitar la costosa autenticación de mensajes de canal segura. (El canal seguro se conserva para que los proveedores de servicios heredados que no implementan [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) puedan seguir funcionando).

El requisito de cifrado impide que las aplicaciones malintencionadas obtengan datos que se pasan entre componentes de software y también protege la integridad de los datos que se envían al dispositivo o desde este.

Los tres métodos siguientes requieren cifrado o descifrado.



| Método                                                                          | Descripción                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | (Aplicación) Cifrado o descifrado, en función de si la aplicación envía o recibe datos. |
| [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | (Proveedor de servicios) Cifrado.                                                                             |
| [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | (Proveedor de servicios) Descifrado.                                                                             |



 

El cifrado y el descifrado se realizan mediante llamadas de método único. El cifrado lo realiza [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) para aplicaciones o [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) para proveedores de servicios. El descifrado lo realiza [**CSecureChannelClient::D ecryptParam**](/previous-versions/bb231586(v=vs.85)) para aplicaciones o [**CSecureChannelServer::D ecryptParam**](/previous-versions/bb231598(v=vs.85)) para proveedores de servicios. Los parámetros son idénticos entre los métodos cliente y servidor.

En los pasos siguientes se muestra cómo cifrar y descifrar datos. (Estos pasos son importantes solo si la aplicación se comunica con un proveedor de servicios heredado que no implementa [IWMDMOperation3::TransferObjectDataOnClearChannel).](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel)

**Cifrado**

1.  Cree la clave MAC para los datos cifrados, como se describe en [Autenticación de mensajes.](message-authentication.md)
2.  Llame **a EncryptParam** con los datos que se cifran para realizar el cifrado en contexto.

En el ejemplo de código siguiente se muestra la implementación de [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)de un proveedor de servicios. Este método crea la clave MAC con los datos para cifrar y el tamaño de los datos, y los envía a la aplicación.


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



**Descifrado**

1.  Llame **a DecryptParam** con los datos que se cifran para realizar el descifrado local.
2.  Compruebe la clave MAC para los datos descifrados, como se describe en [Autenticación de mensajes.](message-authentication.md)

En el ejemplo de código siguiente se muestra la implementación de [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)de un proveedor de servicios. Este método crea la clave MAC con los datos para cifrar y el tamaño de los datos, y los envía a la aplicación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de canales autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 