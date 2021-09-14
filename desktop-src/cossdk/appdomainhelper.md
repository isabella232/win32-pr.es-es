---
description: Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: Clase AppDomainHelper (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073023"
---
# <a name="appdomainhelper-class"></a>AppDomainHelper (clase)

Enlaza un objeto administrado a un dominio de aplicación, que es un entorno aislado donde se ejecutan las aplicaciones.

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Value |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AppDomainHelper                                 |
| ProgID     | L"System.EnterpriseServices.Internal.AppDomainHelper" |
| Interfaces | [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto AppDomainHelper se puede declarar mediante "COMSVCSLib.AppDomainHelper" como nombre de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

