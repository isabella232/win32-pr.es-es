---
title: Recuperar un objeto de una colección
description: Recuperar un objeto de una colección
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8d5bfcba8a1671c7824a4b1356e9c8e1dd7567
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533321"
---
# <a name="retrieving-an-object-from-a-collection"></a>Recuperar un objeto de una colección

El código siguiente recupera la dirección IP de un cliente de una colección de clientes. La variable pClientsCollection apunta a una interfaz [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) para la colección. Consulte [recuperar una colección](/windows/desktop/Nps/sdo-retrieving-a-collection) para obtener información sobre cómo recuperar el objeto de colección.


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ISdoCollection:: Item**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[Recuperación de una colección](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[**VARIANTE**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 