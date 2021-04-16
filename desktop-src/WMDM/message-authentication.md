---
title: Autenticación de mensajes
description: Autenticación de mensajes
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media Administrador de dispositivos, autenticación de mensajes
- Administrador de dispositivos, autenticación de mensajes
- aplicaciones de escritorio, autenticación de mensajes
- proveedores de servicios, autenticación de mensajes
- Guía de programación, autenticación de mensajes
- autenticación de mensajes
- código de autenticación de mensajes (MAC)
- MAC (código de autenticación de mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695242"
---
# <a name="message-authentication"></a>Autenticación de mensajes

La autenticación de mensajes es un proceso que permite a las aplicaciones y a los proveedores de servicios comprobar que los datos que se pasan entre ellos no se han alterado. Windows Media Administrador de dispositivos permite a las aplicaciones y proveedores de servicios realizar la autenticación de mensajes mediante códigos de autenticación de mensajes (Mac). Este es el funcionamiento de la autenticación de MAC:

El remitente de datos, normalmente el proveedor de servicios, pasa uno o más fragmentos de datos a través de una función criptográfica unidireccional que produce una sola firma, el equipo MAC, para todos los datos. A continuación, el remitente envía todas las partes de datos firmadas junto con el equipo MAC al receptor (normalmente la aplicación). El receptor pasa los datos a través de la misma función criptográfica para generar un equipo MAC y lo compara con el equipo MAC que se envió. Si el MAC coincide, los datos no se han modificado.

Para realizar la autenticación de MAC, la aplicación o el proveedor de servicios requiere una clave de cifrado y un certificado coincidente. Para obtener información sobre dónde obtenerlas, consulte [herramientas para el desarrollo](tools-for-development.md).

En los pasos siguientes se describe cómo el remitente firma los datos y, posteriormente, el receptor los comprueba. En Windows Media Administrador de dispositivos, el proveedor de servicios usa la clase [CSecureChannelServer](csecurechannelserver-class.md) para generar los equipos Mac y la aplicación utiliza la clase [CSecureChannelClient](csecurechannelclient-class.md) . Ambas clases proporcionan funciones idénticas con parámetros idénticos, por lo que los pasos siguientes se aplican a ambas clases.

Remitente (normalmente, el proveedor de servicios):

1.  Obtiene los datos que se van a firmar.
2.  Cree un nuevo identificador MAC llamando a **MACInit**.
3.  Agregue un fragmento de datos que se va a firmar al identificador llamando a **MACUpdate**. Esta función acepta el identificador creado anteriormente, además de un fragmento de datos que se debe firmar.
4.  Repita el paso 3 con cada fragmento de datos adicional que se deba firmar. No importa el orden en que se agregan los datos al equipo MAC.
5.  Copie el equipo MAC del identificador a un nuevo búfer de bytes mediante una llamada a **MACFinal**. Esta función acepta el identificador MAC y un búfer que se asignan, y copia el equipo MAC del identificador en el búfer proporcionado.

Al realizar la autenticación de MAC, es importante que tanto el remitente como el receptor estén colocando los mismos datos en el equipo MAC. En el caso de los métodos de aplicación que proporcionan un equipo MAC, normalmente todos los parámetros se incluyen en el valor MAC (excepto en el propio equipo, por supuesto). Por ejemplo, considere el método **IWMDMOperation:: TransferObjectData** :

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

En este método, el equipo MAC incluiría *pdata* y *pdwSize*. Si no incluye ambos parámetros, el equipo MAC que cree no coincidirá con el MAC que se pasa a *abMac*. Un proveedor de servicios debe asegurarse de poner todos los parámetros necesarios en el método de aplicación en el valor MAC.

En el código de C++ siguiente se muestra la creación de un equipo MAC en la implementación de un proveedor de servicios de [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



El receptor (normalmente la aplicación):

Si el receptor no ha implementado la interfaz [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , debe realizar los mismos pasos que el remitente y, a continuación, comparar los dos valores Mac. En el ejemplo de código de C++ siguiente se muestra cómo una aplicación comprobaría el equipo MAC recibido en una llamada a [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) para asegurarse de que el número de serie no se alteró en tránsito.


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar canales autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




