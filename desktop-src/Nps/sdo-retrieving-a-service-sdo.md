---
title: Recuperación de un SDO de servicio
description: Recuperación de un SDO de servicio
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f1ec3f8537cbf6e9a7be82f8152bc764a263093fe0ebeee46ed1499abfd346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618961"
---
# <a name="retrieving-a-service-sdo"></a>Recuperación de un SDO de servicio

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008.

 

El código siguiente recupera un objeto de datos de servidor (SDO) para el servidor de directivas de red .


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a>Observaciones

Debe [conectarse](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) a un equipo para poder llamar a cualquiera de los [**métodos ISdoMachine.**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Adjuntar a un equipo SDO-Enabled cliente](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 