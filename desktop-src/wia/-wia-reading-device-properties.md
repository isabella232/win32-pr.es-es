---
description: Las aplicaciones usan la interfaz IWiaPropertyStorage de un dispositivo para leer y escribir las propiedades de los dispositivos. IWiaPropertyStorage hereda todos los métodos de la interfaz IPropertyStorage del modelo de objetos componentes (COM).
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lectura de las propiedades del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001179"
---
# <a name="reading-device-properties"></a><span data-ttu-id="3492d-104">Lectura de las propiedades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3492d-104">Reading Device Properties</span></span>

<span data-ttu-id="3492d-105">Las aplicaciones usan la interfaz [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) de un dispositivo para leer y escribir las propiedades de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3492d-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="3492d-106">**IWiaPropertyStorage** hereda todos los métodos de la interfaz [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="3492d-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="3492d-107">Las propiedades del dispositivo incluyen información sobre un dispositivo que describe las capacidades y la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3492d-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="3492d-108">Para obtener una lista de estas propiedades, consulte [propiedades del dispositivo](-wia-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3492d-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="3492d-109">Entre las propiedades del dispositivo que se leen con [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) se encuentra el identificador del dispositivo, que se usa para crear un dispositivo de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="3492d-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="3492d-110">Para obtener más información, vea [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span><span class="sxs-lookup"><span data-stu-id="3492d-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="3492d-111">En el ejemplo siguiente se lee el identificador del dispositivo, el nombre del dispositivo y la descripción del dispositivo de la matriz de propiedades del dispositivo, y se imprimen estas propiedades en la consola.</span><span class="sxs-lookup"><span data-stu-id="3492d-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



<span data-ttu-id="3492d-112">En este ejemplo, la aplicación configura matrices de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (**PropSpec** y **PropVar**, respectivamente) para contener información de propiedades.</span><span class="sxs-lookup"><span data-stu-id="3492d-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="3492d-113">Estas matrices se pasan como parámetros en la llamada al método [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del puntero [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**.</span><span class="sxs-lookup"><span data-stu-id="3492d-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="3492d-114">Cada elemento de la matriz **PropSpec** contiene el tipo y el nombre de una propiedad de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3492d-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="3492d-115">Al devolverse, cada elemento de **PropVar** contiene el valor de la propiedad del dispositivo representado por el elemento correspondiente de la matriz **PropSpec** .</span><span class="sxs-lookup"><span data-stu-id="3492d-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="3492d-116">A continuación, la aplicación llama a la propiedad [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del puntero [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pWiaPropertyStorage** para recuperar la información de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3492d-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="3492d-117">La técnica que se usa para leer y establecer las propiedades del dispositivo es la misma que la de las propiedades del elemento, la única diferencia es el tipo del elemento WIA en el que se llama a los métodos adecuados.</span><span class="sxs-lookup"><span data-stu-id="3492d-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="3492d-118">Para obtener una lista de las propiedades de los elementos, vea propiedades de los [elementos](-wia-item-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3492d-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 
