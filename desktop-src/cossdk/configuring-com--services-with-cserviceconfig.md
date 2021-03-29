---
description: Configuración de servicios COM+ con CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configuración de servicios COM+ con CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807189"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Configuración de servicios COM+ con CServiceConfig

La clase [**CServiceConfig**](cserviceconfig.md) se utiliza para configurar los servicios com+ que se pueden usar sin componentes. Agrega el contador de referencias de subprocesamiento libre, por lo que se puede usar en distintos apartamentos. Para configurar un servicio individual, debe llamar a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz asociada con el servicio y, a continuación, llamar a los métodos de esa interfaz para establecer la configuración adecuada. En la tabla siguiente se describen las interfaces que se implementan a través de la clase **CServiceConfig** .



| Interfaz                                                                         | Descripción                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | La interfaz predeterminada para la clase. Se usa para inicializar rápidamente muchos de los servicios COM+.<br/>                                                                                              |
| [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Se utiliza para configurar la información intrínseca del integrador de transacciones COM (COMTI). COMTI permite a los desarrolladores integrar programas de transacciones basados en un gran sistema (mainframe) con aplicaciones basadas en componentes.<br/> |
| [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | Se utiliza para configurar la información intrínseca de Internet Information Services (IIS).<br/>                                                                                                             |
| [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Se utiliza para configurar el modo en que se usan las particiones COM+ con los servicios.<br/>                                                                                                                             |
| [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Se utiliza para configurar ensamblados en paralelo.<br/>                                                                                                                                                    |
| [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Se utiliza para configurar los servicios de sincronización de COM+.<br/>                                                                                                                                              |
| [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Se utiliza para configurar el grupo de subprocesos para el servicio COM+. El grupo de subprocesos solo se puede configurar cuando se usa la función [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .<br/>                          |
| [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Se usa para configurar la propiedad Tracker. Tracker es un mecanismo de informes que usa el código de supervisión para ver qué código se está ejecutando cuando.<br/>                                                         |
| [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Se utiliza para configurar el servicio de transacciones de COM+.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

No corresponde.

## <a name="cc"></a>C/C++

En el siguiente fragmento de código se muestra cómo crear y configurar un objeto [**CServiceConfig**](cserviceconfig.md) para utilizar transacciones com+.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Usar los servicios COM+ a través de CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Uso de los servicios COM+ a través de CoEnterServiceDomain y CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

