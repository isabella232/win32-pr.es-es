---
title: Acceso a atributos con la interfaz IDirectoryObject
description: La interfaz IDirectoryObject proporciona una aplicación cliente escrita en C y C++ con acceso directo a los objetos de servicio de directorio.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Obtener acceso a atributos con la interfaz IDirectoryObject ADSI
- IDirectoryObject ADSI, acceso a atributos con
- ADSI ADSI, usar, uso de la interfaz IDirectoryObject para obtener acceso a atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993881"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Acceso a atributos con la interfaz IDirectoryObject

La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) proporciona una aplicación cliente escrita en C y C++ con acceso directo a los objetos de servicio de directorio. La interfaz permite el acceso por medio de un protocolo de red directo, en lugar de hacerlo a través de la caché de atributos ADSI. En lugar de las propiedades admitidas por la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** proporciona métodos que admiten un subconjunto crítico de los métodos de mantenimiento de un objeto y proporcionan acceso a sus atributos. Con **IDirectoryObject**, un cliente puede obtener o establecer cualquier número de atributos de objeto con una llamada al método. A diferencia de los métodos de automatización correspondientes, que se procesan por lotes, los de **IDirectoryObject** se ejecutan cuando se llama a. Dado que los métodos de esta interfaz no requieren la creación de una instancia de un objeto de directorio de automatización, la sobrecarga de rendimiento es pequeña.

Los clientes escritos en lenguajes como C y C++ deben usar los métodos de la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para optimizar el rendimiento y aprovechar las interfaces de servicio de directorio nativo. Los clientes de Automation no pueden usar **IDirectoryObject**. En su lugar, deben utilizar la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .

El método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera atributos con valores únicos y múltiples. Este método toma una lista de atributos solicitados y devuelve una estructura [**ADS \_ ATTR \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) . ADSI asigna esta estructura; el autor de la llamada debe liberar esta memoria cuando ya no sea necesaria con la función [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

El orden de los valores de atributo devueltos no es necesariamente el mismo que el orden en el que se solicitaron los atributos. Por lo tanto, es necesario comparar los nombres de atributo devueltos de ADSI.

> [!Note]  
> La estructura de [**\_ \_ información del atributo ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) no devuelve todos los atributos solicitados. Solo los atributos que contienen valores forman parte de la estructura devuelta.

 

El número de atributos devueltos viene determinado por el parámetro *dwNumberAttributes* pasado al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .

En el ejemplo de código siguiente se enlaza a un objeto y se usa el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar los atributos del objeto.


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




