---
description: Los proveedores pueden llamar a métodos implementados por WMI desde sus implementaciones de método.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Realizar llamadas a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082695"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="53698-103">Realizar llamadas a WMI</span><span class="sxs-lookup"><span data-stu-id="53698-103">Making Calls to WMI</span></span>

<span data-ttu-id="53698-104">Los proveedores pueden llamar a métodos implementados por WMI desde sus implementaciones de método.</span><span class="sxs-lookup"><span data-stu-id="53698-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="53698-105">Sin embargo, existen consideraciones especiales cuando un proveedor llama a la implementación WMI de un método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) desde su propia implementación del mismo método.</span><span class="sxs-lookup"><span data-stu-id="53698-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="53698-106">Estas consideraciones son importantes independientemente de si el proveedor llama a la versión sincrónica o asincrónica del método.</span><span class="sxs-lookup"><span data-stu-id="53698-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="53698-107">Cada método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que un proveedor puede implementar tiene un parámetro *pCtx* , un puntero a una implementación de la interfaz [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="53698-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="53698-108">Cuando WMI llama al proveedor, WMI pasa un puntero válido en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="53698-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="53698-109">Un proveedor siempre debe pasar este mismo puntero en cualquier llamada a WMI que realicen mientras se atienden las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="53698-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="53698-110">Descuidarse de establecer *pCtx* correctamente puede hacer que WMI inicie un bucle infinito.</span><span class="sxs-lookup"><span data-stu-id="53698-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="53698-111">En el ejemplo de código siguiente se muestra la manera correcta de llamar a la implementación WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) desde dentro de una implementación de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="53698-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="53698-112">El ejemplo de código de C++ de este tema requiere las siguientes referencias e \# incluir instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="53698-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="53698-113">Los proveedores de instancia, clase y propiedad no deben emitir llamadas a WMI que soliciten la modificación de los datos mientras atienden una solicitud de lectura.</span><span class="sxs-lookup"><span data-stu-id="53698-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="53698-114">Los únicos proveedores que son excepciones a esta regla son los proveedores de inserciones.</span><span class="sxs-lookup"><span data-stu-id="53698-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="53698-115">Un proveedor de inserciones es un proveedor de clases que almacena los datos en el repositorio WMI y se basa en WMI para controlar las solicitudes de los clientes.</span><span class="sxs-lookup"><span data-stu-id="53698-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="53698-116">Mientras se atiende una solicitud de lectura, un proveedor de inserciones puede actualizar el repositorio WMI, pero debe establecer el parámetro *lFlags* en la marca WBEM de la llamada a **\_ \_ Owner \_** en la llamada a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) adecuada.</span><span class="sxs-lookup"><span data-stu-id="53698-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="53698-117">Los proveedores de eventos no deben realizar ningún cambio de clase mientras atienden una llamada.</span><span class="sxs-lookup"><span data-stu-id="53698-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="53698-118">Tampoco pueden emitir llamadas relacionadas con eventos, como modificar un filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="53698-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53698-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="53698-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53698-120">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="53698-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="53698-121">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="53698-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="53698-122">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="53698-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



