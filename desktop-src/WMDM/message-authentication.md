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
# <a name="message-authentication"></a><span data-ttu-id="7460a-111">Autenticación de mensajes</span><span class="sxs-lookup"><span data-stu-id="7460a-111">Message Authentication</span></span>

<span data-ttu-id="7460a-112">La autenticación de mensajes es un proceso que permite a las aplicaciones y a los proveedores de servicios comprobar que los datos que se pasan entre ellos no se han alterado.</span><span class="sxs-lookup"><span data-stu-id="7460a-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="7460a-113">Windows Media Administrador de dispositivos permite a las aplicaciones y proveedores de servicios realizar la autenticación de mensajes mediante códigos de autenticación de mensajes (Mac).</span><span class="sxs-lookup"><span data-stu-id="7460a-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="7460a-114">Este es el funcionamiento de la autenticación de MAC:</span><span class="sxs-lookup"><span data-stu-id="7460a-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="7460a-115">El remitente de datos, normalmente el proveedor de servicios, pasa uno o más fragmentos de datos a través de una función criptográfica unidireccional que produce una sola firma, el equipo MAC, para todos los datos.</span><span class="sxs-lookup"><span data-stu-id="7460a-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="7460a-116">A continuación, el remitente envía todas las partes de datos firmadas junto con el equipo MAC al receptor (normalmente la aplicación).</span><span class="sxs-lookup"><span data-stu-id="7460a-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="7460a-117">El receptor pasa los datos a través de la misma función criptográfica para generar un equipo MAC y lo compara con el equipo MAC que se envió.</span><span class="sxs-lookup"><span data-stu-id="7460a-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="7460a-118">Si el MAC coincide, los datos no se han modificado.</span><span class="sxs-lookup"><span data-stu-id="7460a-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="7460a-119">Para realizar la autenticación de MAC, la aplicación o el proveedor de servicios requiere una clave de cifrado y un certificado coincidente.</span><span class="sxs-lookup"><span data-stu-id="7460a-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="7460a-120">Para obtener información sobre dónde obtenerlas, consulte [herramientas para el desarrollo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="7460a-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="7460a-121">En los pasos siguientes se describe cómo el remitente firma los datos y, posteriormente, el receptor los comprueba.</span><span class="sxs-lookup"><span data-stu-id="7460a-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="7460a-122">En Windows Media Administrador de dispositivos, el proveedor de servicios usa la clase [CSecureChannelServer](csecurechannelserver-class.md) para generar los equipos Mac y la aplicación utiliza la clase [CSecureChannelClient](csecurechannelclient-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7460a-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="7460a-123">Ambas clases proporcionan funciones idénticas con parámetros idénticos, por lo que los pasos siguientes se aplican a ambas clases.</span><span class="sxs-lookup"><span data-stu-id="7460a-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="7460a-124">Remitente (normalmente, el proveedor de servicios):</span><span class="sxs-lookup"><span data-stu-id="7460a-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="7460a-125">Obtiene los datos que se van a firmar.</span><span class="sxs-lookup"><span data-stu-id="7460a-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="7460a-126">Cree un nuevo identificador MAC llamando a **MACInit**.</span><span class="sxs-lookup"><span data-stu-id="7460a-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="7460a-127">Agregue un fragmento de datos que se va a firmar al identificador llamando a **MACUpdate**.</span><span class="sxs-lookup"><span data-stu-id="7460a-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="7460a-128">Esta función acepta el identificador creado anteriormente, además de un fragmento de datos que se debe firmar.</span><span class="sxs-lookup"><span data-stu-id="7460a-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="7460a-129">Repita el paso 3 con cada fragmento de datos adicional que se deba firmar.</span><span class="sxs-lookup"><span data-stu-id="7460a-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="7460a-130">No importa el orden en que se agregan los datos al equipo MAC.</span><span class="sxs-lookup"><span data-stu-id="7460a-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="7460a-131">Copie el equipo MAC del identificador a un nuevo búfer de bytes mediante una llamada a **MACFinal**.</span><span class="sxs-lookup"><span data-stu-id="7460a-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="7460a-132">Esta función acepta el identificador MAC y un búfer que se asignan, y copia el equipo MAC del identificador en el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="7460a-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="7460a-133">Al realizar la autenticación de MAC, es importante que tanto el remitente como el receptor estén colocando los mismos datos en el equipo MAC.</span><span class="sxs-lookup"><span data-stu-id="7460a-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="7460a-134">En el caso de los métodos de aplicación que proporcionan un equipo MAC, normalmente todos los parámetros se incluyen en el valor MAC (excepto en el propio equipo, por supuesto).</span><span class="sxs-lookup"><span data-stu-id="7460a-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="7460a-135">Por ejemplo, considere el método **IWMDMOperation:: TransferObjectData** :</span><span class="sxs-lookup"><span data-stu-id="7460a-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="7460a-136">En este método, el equipo MAC incluiría *pdata* y *pdwSize*.</span><span class="sxs-lookup"><span data-stu-id="7460a-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="7460a-137">Si no incluye ambos parámetros, el equipo MAC que cree no coincidirá con el MAC que se pasa a *abMac*.</span><span class="sxs-lookup"><span data-stu-id="7460a-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="7460a-138">Un proveedor de servicios debe asegurarse de poner todos los parámetros necesarios en el método de aplicación en el valor MAC.</span><span class="sxs-lookup"><span data-stu-id="7460a-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="7460a-139">En el código de C++ siguiente se muestra la creación de un equipo MAC en la implementación de un proveedor de servicios de [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span><span class="sxs-lookup"><span data-stu-id="7460a-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


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



<span data-ttu-id="7460a-140">El receptor (normalmente la aplicación):</span><span class="sxs-lookup"><span data-stu-id="7460a-140">The receiver (typically the application):</span></span>

<span data-ttu-id="7460a-141">Si el receptor no ha implementado la interfaz [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , debe realizar los mismos pasos que el remitente y, a continuación, comparar los dos valores Mac.</span><span class="sxs-lookup"><span data-stu-id="7460a-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="7460a-142">En el ejemplo de código de C++ siguiente se muestra cómo una aplicación comprobaría el equipo MAC recibido en una llamada a [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) para asegurarse de que el número de serie no se alteró en tránsito.</span><span class="sxs-lookup"><span data-stu-id="7460a-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7460a-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7460a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7460a-144">**Usar canales autenticados seguros**</span><span class="sxs-lookup"><span data-stu-id="7460a-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




