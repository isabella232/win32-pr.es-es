---
title: Colecciones de dispositivos devueltas por búsquedas sincrónicas
description: Las colecciones de dispositivos son objetos que contienen uno o más objetos de dispositivo. Una colección de dispositivos expone la interfaz IUPnPDevices que proporciona métodos y propiedades para atravesar la colección y extraer objetos de dispositivo individuales.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149479"
---
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="18b3b-104">Colecciones de dispositivos devueltas por búsquedas sincrónicas</span><span class="sxs-lookup"><span data-stu-id="18b3b-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="18b3b-105">Las colecciones de dispositivos son objetos que contienen uno o más objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3b-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="18b3b-106">Una colección de dispositivos expone la interfaz [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) que proporciona métodos y propiedades para atravesar la colección y extraer objetos de dispositivo individuales.</span><span class="sxs-lookup"><span data-stu-id="18b3b-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="18b3b-107">Ejemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="18b3b-107">VBScript Example</span></span>

<span data-ttu-id="18b3b-108">Las aplicaciones de VBScript pueden tener acceso a los objetos de la colección de dos maneras.</span><span class="sxs-lookup"><span data-stu-id="18b3b-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="18b3b-109">En primer lugar, pueden atravesar los elementos secuencialmente mediante un elemento for...</span><span class="sxs-lookup"><span data-stu-id="18b3b-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="18b3b-110">cada... siguiente, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="18b3b-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="18b3b-111">En este ejemplo, se supone que la variable Devices se ha inicializado con el resultado de una búsqueda anterior.</span><span class="sxs-lookup"><span data-stu-id="18b3b-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="18b3b-112">El bucle recorre los objetos de dispositivo de la colección, asignando la variable deviceObj el valor de cada objeto de dispositivo a su vez.</span><span class="sxs-lookup"><span data-stu-id="18b3b-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="18b3b-113">El cuerpo del bucle puede contener código que procese el objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3b-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="18b3b-114">Ejemplo de C++</span><span class="sxs-lookup"><span data-stu-id="18b3b-114">C++ Example</span></span>

<span data-ttu-id="18b3b-115">En el ejemplo siguiente se muestra el código de C++ necesario para tener acceso a los objetos de una colección de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3b-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="18b3b-116">La función que se muestra, **TraverseCollection**, recibe un puntero a la interfaz [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="18b3b-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="18b3b-117">Este puntero de interfaz puede ser devuelto por el método [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) u otros métodos **Find** del objeto Finder del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3b-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



<span data-ttu-id="18b3b-118">El primer paso es solicitar un nuevo enumerador para la colección mediante la propiedad [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="18b3b-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="18b3b-119">Esto devuelve un enumerador como la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="18b3b-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18b3b-120">El código de ejemplo invoca a [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener la interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="18b3b-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="18b3b-121">A continuación, el código de ejemplo establece el enumerador al principio de la colección invocando el método [**IEnumVARIANT:: RESET**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) .</span><span class="sxs-lookup"><span data-stu-id="18b3b-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="18b3b-122">Por último, el código de ejemplo invoca el método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para recorrer la colección.</span><span class="sxs-lookup"><span data-stu-id="18b3b-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="18b3b-123">Los objetos de dispositivo de la colección están contenidos en estructuras **variantes** .</span><span class="sxs-lookup"><span data-stu-id="18b3b-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="18b3b-124">Estas estructuras contienen punteros a interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en los objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18b3b-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="18b3b-125">Para obtener la interfaz [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , el código de ejemplo invoca **QueryInterface** en la interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="18b3b-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 