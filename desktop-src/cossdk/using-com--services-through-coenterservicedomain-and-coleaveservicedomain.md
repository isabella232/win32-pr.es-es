---
description: Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153254"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) se usan juntos para rodear un área de código que se ejecuta en su propio contexto y puede usar los servicios com+ sin necesidad de componentes com+. Los servicios COM+ que se usan en este contexto se configuran mediante el objeto [**CServiceConfig**](cserviceconfig.md) que se pasa a **CoEnterServiceDomain**. El código que está rodeado por **CoEnterServiceDomain** y **CoLeaveServiceDomain** se comporta como si fuera un método al que se llama en un objeto creado dentro de este contexto.

Una aplicación de scripting puede usar este par de funciones para proporcionar compatibilidad en tiempo de ejecución de los servicios COM+ sin componentes. Por ejemplo, se puede desarrollar una aplicación de scripting para proporcionar etiquetas que permitan a los escritores de scripts entrar y salir de un dominio de servicio dentro del script. Cuando el motor de scripting procesa el script y encuentra las etiquetas, puede llamar a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) con un objeto [**CServiceConfig**](cserviceconfig.md) preconfigurado, ejecutar el código necesario y, después, llamar a [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

En el fragmento de código siguiente se muestra cómo usar los servicios COM+ entre las llamadas a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) y [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain). Con el fin de ser breves se omite el control de errores. Este fragmento de código usa el objeto [**CServiceConfig**](cserviceconfig.md) que se creó y configuró en configuración de los [servicios com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Configuración de servicios COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Usar los servicios COM+ a través de CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



