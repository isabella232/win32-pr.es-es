---
description: Apertura de un servicio
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Apertura de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423925"
---
# <a name="opening-a-service"></a><span data-ttu-id="11924-103">Apertura de un servicio</span><span class="sxs-lookup"><span data-stu-id="11924-103">Opening a Service</span></span>

<span data-ttu-id="11924-104">Para que la aplicación pueda realizar operaciones en un servicio, por ejemplo, enumerar contenido o recuperar descripciones de los métodos o eventos admitidos, debe abrir el servicio.</span><span class="sxs-lookup"><span data-stu-id="11924-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="11924-105">En la aplicación WpdServicesApiSample, esta tarea se muestra en el módulo ServiceEnumeration.cpp mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="11924-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



| <span data-ttu-id="11924-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="11924-106">Interface</span></span>                                                              | <span data-ttu-id="11924-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="11924-107">Description</span></span>                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="11924-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="11924-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="11924-109">Se usa para enumerar los servicios de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11924-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="11924-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="11924-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="11924-111">Se usa para abrir una conexión a un servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11924-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="11924-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="11924-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="11924-113">Se usa para contener la información de cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11924-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="11924-114">El método que abre un servicio [**es IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)</span><span class="sxs-lookup"><span data-stu-id="11924-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="11924-115">Este método toma dos argumentos: un identificador plug-and-play (PnP) para el servicio y un objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contiene la información de cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11924-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="11924-116">Para obtener un identificador PnP para un servicio determinado, la aplicación llama al método [**IPortableDeviceServiceManager::GetDeviceServices.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)</span><span class="sxs-lookup"><span data-stu-id="11924-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="11924-117">Este método recupera una matriz de identificadores PnP para los servicios de un GUID de categoría de servicio (por ejemplo, contactos DE SERVICIO).</span><span class="sxs-lookup"><span data-stu-id="11924-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="11924-118">La aplicación de servicio de ejemplo recupera un identificador PnP para los servicios contacts dentro del método **EnumerateContactsServices** del módulo ServiceEnumeration.cpp.</span><span class="sxs-lookup"><span data-stu-id="11924-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="11924-119">El siguiente ejemplo de código se toma de este método.</span><span class="sxs-lookup"><span data-stu-id="11924-119">The following code sample is taken from this method.</span></span>


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



<span data-ttu-id="11924-120">Una vez que la aplicación recupera el identificador pnP del servicio, puede configurar la información del cliente y llamar a [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="11924-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="11924-121">En la aplicación de ejemplo, se llama a este método **en ChooseDeviceService** en el módulo ServiceEnumeration.cpp.</span><span class="sxs-lookup"><span data-stu-id="11924-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="11924-122">[**IPortableDeviceService admite**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) dos CLID para **CoCreateInstance.**</span><span class="sxs-lookup"><span data-stu-id="11924-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="11924-123">**CLSID \_ PortableDeviceService** devuelve un **puntero IPortableDeviceService** que no agrega el serializador de subproceso libre; **CLSID \_ PortableDeviceServiceFTM** es un nuevo CLSID que devuelve un puntero **IPortableDeviceService** que agrega el serializador de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="11924-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="11924-124">En caso contrario, ambos punteros admiten la misma funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="11924-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="11924-125">Las aplicaciones que se usan en los departamentos de subproceso único deben usar **CLSID \_ PortableDeviceServiceFTM,** ya que esto elimina la sobrecarga de la serialización de punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="11924-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="11924-126">**CLSID \_ PortableDeviceService sigue** siendo compatible con las aplicaciones heredadas.</span><span class="sxs-lookup"><span data-stu-id="11924-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a><span data-ttu-id="11924-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11924-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11924-128">**IPortableDeviceService (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="11924-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="11924-129">**IPortableDeviceValues (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="11924-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="11924-130">**IPortableDeviceServiceManager (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="11924-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="11924-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="11924-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



