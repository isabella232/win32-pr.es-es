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
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="abd97-106">Acceso a atributos con la interfaz IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="abd97-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="abd97-107">La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) proporciona una aplicación cliente escrita en C y C++ con acceso directo a los objetos de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="abd97-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="abd97-108">La interfaz permite el acceso por medio de un protocolo de red directo, en lugar de hacerlo a través de la caché de atributos ADSI.</span><span class="sxs-lookup"><span data-stu-id="abd97-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="abd97-109">En lugar de las propiedades admitidas por la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** proporciona métodos que admiten un subconjunto crítico de los métodos de mantenimiento de un objeto y proporcionan acceso a sus atributos.</span><span class="sxs-lookup"><span data-stu-id="abd97-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="abd97-110">Con **IDirectoryObject**, un cliente puede obtener o establecer cualquier número de atributos de objeto con una llamada al método.</span><span class="sxs-lookup"><span data-stu-id="abd97-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="abd97-111">A diferencia de los métodos de automatización correspondientes, que se procesan por lotes, los de **IDirectoryObject** se ejecutan cuando se llama a.</span><span class="sxs-lookup"><span data-stu-id="abd97-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="abd97-112">Dado que los métodos de esta interfaz no requieren la creación de una instancia de un objeto de directorio de automatización, la sobrecarga de rendimiento es pequeña.</span><span class="sxs-lookup"><span data-stu-id="abd97-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="abd97-113">Los clientes escritos en lenguajes como C y C++ deben usar los métodos de la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para optimizar el rendimiento y aprovechar las interfaces de servicio de directorio nativo.</span><span class="sxs-lookup"><span data-stu-id="abd97-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="abd97-114">Los clientes de Automation no pueden usar **IDirectoryObject**.</span><span class="sxs-lookup"><span data-stu-id="abd97-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="abd97-115">En su lugar, deben utilizar la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="abd97-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="abd97-116">El método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera atributos con valores únicos y múltiples.</span><span class="sxs-lookup"><span data-stu-id="abd97-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="abd97-117">Este método toma una lista de atributos solicitados y devuelve una estructura [**ADS \_ ATTR \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) .</span><span class="sxs-lookup"><span data-stu-id="abd97-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="abd97-118">ADSI asigna esta estructura; el autor de la llamada debe liberar esta memoria cuando ya no sea necesaria con la función [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="abd97-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="abd97-119">El orden de los valores de atributo devueltos no es necesariamente el mismo que el orden en el que se solicitaron los atributos.</span><span class="sxs-lookup"><span data-stu-id="abd97-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="abd97-120">Por lo tanto, es necesario comparar los nombres de atributo devueltos de ADSI.</span><span class="sxs-lookup"><span data-stu-id="abd97-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="abd97-121">La estructura de [**\_ \_ información del atributo ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) no devuelve todos los atributos solicitados.</span><span class="sxs-lookup"><span data-stu-id="abd97-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="abd97-122">Solo los atributos que contienen valores forman parte de la estructura devuelta.</span><span class="sxs-lookup"><span data-stu-id="abd97-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="abd97-123">El número de atributos devueltos viene determinado por el parámetro *dwNumberAttributes* pasado al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="abd97-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="abd97-124">En el ejemplo de código siguiente se enlaza a un objeto y se usa el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar los atributos del objeto.</span><span class="sxs-lookup"><span data-stu-id="abd97-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


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



 

 




