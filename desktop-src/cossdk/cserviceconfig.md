---
description: Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a CoCreateActivity o CoEnterServiceDomain.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Clase CServiceConfig (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705271"
---
# <a name="cserviceconfig-class"></a>Clase CServiceConfig

Especifica y configura los servicios que deben estar activos en el dominio de servicio especificado al llamar a [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ CServiceConfig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ProgID     | L "COMSVCS. CServiceConfig"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces | [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a>Cuándo se usa

Utilice esta clase para configurar los servicios que desea usar. [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) y [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) permiten usar los servicios configurados por esta clase sin necesidad de asociar esos servicios a un componente antes de usarlos.

Esta clase no está diseñada para utilizarse en Visual Basic.

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Los objetos de los que se ha creado una instancia de la clase **CServiceConfig** agregan el contador de referencias de subprocesamiento libre para que puedan almacenarse en tiempo de ejecución del sistema y reutilizarse en distintos apartamentos.

Para configurar un servicio individual, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz asociada con el servicio y, a continuación, llame a los métodos de esa interfaz para establecer la configuración adecuada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP1 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[**CoCreateFreeThreadedMarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Servicios COM+ sin componentes](com--services-without-components.md)
</dt> </dl>

 

