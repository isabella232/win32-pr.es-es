---
description: Apertura de un servicio
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Apertura de un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bcccc6c3769173bfee72e73d7cbf68435b0ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546059"
---
# <a name="opening-a-service"></a>Apertura de un servicio

Para que la aplicación pueda realizar operaciones en un servicio, por ejemplo, enumerar contenido o recuperar descripciones de métodos o eventos admitidos, debe abrir el servicio. En la aplicación WpdServicesApiSample, esta tarea se muestra en el módulo ServiceEnumeration. cpp con las interfaces descritas en la tabla siguiente.



|                                                                        |                                                    |
|------------------------------------------------------------------------|----------------------------------------------------|
| Interfaz                                                              | Descripción                                        |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Se usa para enumerar los servicios en un dispositivo.        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Se utiliza para abrir una conexión a un servicio de dispositivo.     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Se utiliza para almacenar la información de cliente de la aplicación. |



 

El método que abre un servicio es [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open). Este método toma dos argumentos: un identificador de plug and Play (PnP) para el servicio y un objeto [**IPortableDeviceValues**](iportabledevicevalues.md) que contiene la información de cliente de la aplicación.

Para obtener un identificador de PnP para un servicio determinado, la aplicación llama al método [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) . Este método recupera una matriz de identificadores de PnP para los servicios de un GUID de categoría de servicio (por ejemplo, contactos de servicio).

La aplicación de servicio de ejemplo recupera un identificador de PnP para los servicios de contactos en el método **EnumerateContactsServices** del módulo ServiceEnumeration. cpp. El siguiente ejemplo de código se toma de este método.


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



Una vez que la aplicación recupera el identificador de PnP para el servicio, puede configurar la información del cliente y llamar a [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).

En la aplicación de ejemplo, se llama a este método dentro de **ChooseDeviceService** en el módulo ServiceEnumeration. cpp.

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) admite dos CLSID para **CoCreateInstance**. **CLSID \_ de PortableDeviceService** devuelve un puntero **IPortableDeviceService** que no agrega el contador de referencias de subprocesamiento libre; **CLSID \_ de PortableDeviceServiceFTM** es un nuevo CLSID que devuelve un puntero **IPortableDeviceService** que agrega el contador de referencias de subprocesamiento libre. Ambos punteros admiten la misma funcionalidad en caso contrario.

Las aplicaciones que residen en apartamentos de un solo subproceso deben usar **CLSID \_ PortableDeviceServiceFTM** , ya que esto elimina la sobrecarga que supone la serialización del puntero de interfaz. **CLSID \_ de PortableDeviceService** sigue siendo compatible con las aplicaciones heredadas.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Interfaz IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Interfaz IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



