---
description: El siguiente procedimiento proporciona una breve introducción al proceso de compilación.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Compilar un comando de APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275798"
---
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="9208a-103">Compilar un comando de APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="9208a-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="9208a-104">Para agregar funcionalidad a un proveedor de servicios, debe saber cómo se crea una [*unidad de datos de protocolo de aplicación*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (APDU) dentro de los archivos DLL del proveedor de servicios base.</span><span class="sxs-lookup"><span data-stu-id="9208a-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="9208a-105">El siguiente procedimiento proporciona una breve introducción al proceso de compilación.</span><span class="sxs-lookup"><span data-stu-id="9208a-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="9208a-106">El ejemplo que se incluye aquí no es necesariamente completo; para obtener más información, vea las aplicaciones de ejemplo y los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="9208a-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="9208a-107">**Para compilar un comando de APDU ISO7816-4**</span><span class="sxs-lookup"><span data-stu-id="9208a-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="9208a-108">Cree un objeto [**ISCardCmd**](iscardcmd.md) y un objeto [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="9208a-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    <span data-ttu-id="9208a-109">La interfaz [**ISCardCmd**](iscardcmd.md) contiene dos búferes **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="9208a-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="9208a-110">Un búfer contiene la cadena de comando APDU real (además de los datos que se van a enviar con el comando).</span><span class="sxs-lookup"><span data-stu-id="9208a-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="9208a-111">El otro contiene cualquier información de respuesta devuelta por la tarjeta después de la ejecución del comando.</span><span class="sxs-lookup"><span data-stu-id="9208a-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="9208a-112">Con estos objetos, cree un comando ISO7816-4 válido como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="9208a-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="9208a-113">Este es el código que se usa en el método [**GetChallenge**](iscardiso7816-getchallenge.md) :</span><span class="sxs-lookup"><span data-stu-id="9208a-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    <span data-ttu-id="9208a-114">El método [**ISCardISO7816:: GetChallenge**](iscardiso7816-getchallenge.md) usa el método [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) para compilar las APDU solicitadas.</span><span class="sxs-lookup"><span data-stu-id="9208a-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="9208a-115">Para ello, se escribe la información adecuada en el búfer APDU [**ISCardCmd**](iscardcmd.md) en la siguiente instrucción:</span><span class="sxs-lookup"><span data-stu-id="9208a-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="9208a-116">Con el objeto [**ISCardCmd**](iscardcmd.md) compilado, realice una transacción con la tarjeta, interprete los resultados y continúe.</span><span class="sxs-lookup"><span data-stu-id="9208a-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="9208a-117">Expandir más allá de ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="9208a-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="9208a-118">El método recomendado para expandir el proceso de compilación o ejecución del proveedor de servicios descrito anteriormente es crear un nuevo objeto COM.</span><span class="sxs-lookup"><span data-stu-id="9208a-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="9208a-119">Este objeto COM debe admitir una nueva interfaz que permita la creación de comandos no ISO7816-4 y debe agregar la interfaz [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="9208a-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="9208a-120">Ejemplo de creación de un comando de APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="9208a-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="9208a-121">En el ejemplo siguiente se muestra el código utilizado en el procedimiento anterior.</span><span class="sxs-lookup"><span data-stu-id="9208a-121">The following example shows the code used in the procedure above.</span></span>


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
