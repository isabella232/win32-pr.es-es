---
description: La función CoCreateActivity se usa para enviar el trabajo por lotes al sistema COM+. Permite que las aplicaciones basadas en scripts admitan una configuración de servicio COM+ para toda la aplicación.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Uso de servicios COM+ a través de CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5452c99fa431e7c1927646eec7ad9b5e5fa930f3ba7d0bf242df7690325db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128667"
---
# <a name="using-com-services-through-cocreateactivity"></a>Uso de servicios COM+ a través de CoCreateActivity

La [**función CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) se usa para enviar el trabajo por lotes al sistema COM+. Permite que las aplicaciones basadas en scripts admitan una configuración de servicio COM+ para toda la aplicación.

Los servicios COM+ deseados se configuran a través [**de un objeto CServiceConfig**](cserviceconfig.md) que se pasa a la función . La función crea un objeto de actividad y devuelve la [**interfaz IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) de ese objeto. El trabajo por lotes se puede enviar de forma sincrónica o asincrónica mediante los métodos [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) o [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivamente. Se pasa un puntero a una interfaz [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) a cada uno de estos métodos y el desarrollador implementa el trabajo por lotes en el método [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) de la **interfaz IServiceCall.**

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra cómo usar servicios COM+ a través [**de CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). Con el fin de ser breves se omite el control de errores. Este fragmento de código usa el [**objeto CServiceConfig**](cserviceconfig.md) que se creó y configuró en Configuración de servicios [COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Configuración de servicios COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Uso de servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



