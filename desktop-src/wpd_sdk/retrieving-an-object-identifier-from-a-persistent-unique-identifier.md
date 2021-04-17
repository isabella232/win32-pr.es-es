---
description: Recuperar un identificador de objeto de un identificador único persistente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recuperar un identificador de objeto de un identificador único persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716576"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="a5e0b-103">Recuperar un identificador de objeto de un identificador único persistente</span><span class="sxs-lookup"><span data-stu-id="a5e0b-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="a5e0b-104">Solo se garantiza que los identificadores de objeto son únicos para una sesión de dispositivo determinada; Si el usuario establece una nueva conexión, es posible que los identificadores de una sesión anterior no coincidan con los identificadores de la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="a5e0b-105">Para resolver este problema, la API de WPD admite identificadores únicos persistentes (PUID), que se conservan en las sesiones de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="a5e0b-106">Algunos dispositivos almacenan sus PUID de forma nativa con un objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="a5e0b-107">Otros pueden generar el PUID basándose en un hash de los datos del objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="a5e0b-108">Otros pueden tratar identificadores de objeto como PUID (porque pueden garantizar que estos identificadores nunca cambian).</span><span class="sxs-lookup"><span data-stu-id="a5e0b-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="a5e0b-109">La función GetObjectIdentifierFromPersistentUniqueIdentifier del módulo ContentProperties. cpp muestra la recuperación de un identificador de objeto para un PUID determinado.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="a5e0b-110">La aplicación puede recuperar un identificador de objeto para un PUID correspondiente mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="a5e0b-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="a5e0b-111">Interface</span></span>                                                                                      | <span data-ttu-id="a5e0b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e0b-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5e0b-113">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="a5e0b-114">Proporciona acceso al método de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="a5e0b-115">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="a5e0b-116">Se utiliza para almacenar el identificador de objeto y el identificador único persistente (PUID) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="a5e0b-117">La primera tarea que realiza la aplicación de ejemplo es obtener un PUID del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="a5e0b-118">Después, la aplicación de ejemplo recupera un objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que se usará para invocar el método [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="a5e0b-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="a5e0b-119">A continuación, crea un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contendrá el PUID proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="a5e0b-120">Una vez realizados los tres pasos anteriores, el ejemplo está listo para recuperar el identificador de objeto que coincide con el PUID proporcionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="a5e0b-121">Esto se logra mediante una llamada al método [**IPortableDeviceContent:: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="a5e0b-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="a5e0b-122">Antes de llamar a este método, el ejemplo Inicializa una estructura PROPVARIANT, escribe el PUID proporcionado por el usuario en esta estructura y lo agrega al objeto IPortableDevicePropVariantCollection en el que pPersistentUniqueIDs apunta.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="a5e0b-123">Este puntero se pasa como primer argumento al método GetObjectIDsFromPersistentUniqueIDs.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="a5e0b-124">El segundo argumento de GetObjectIDsFromPersistentUniqueIDs es un objeto IPortableDevicePropVariantCollection que recibe el identificador de objeto coincidente.</span><span class="sxs-lookup"><span data-stu-id="a5e0b-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a5e0b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5e0b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e0b-126">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="a5e0b-127">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="a5e0b-128">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="a5e0b-129">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="a5e0b-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



