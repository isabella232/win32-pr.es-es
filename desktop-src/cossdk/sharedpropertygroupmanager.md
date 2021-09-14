---
description: Crea grupos de propiedades compartidas y para obtener acceso a los grupos de propiedades compartidos existentes.
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: Clase SharedPropertyGroupManager (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361659"
---
# <a name="sharedpropertygroupmanager-class"></a>SharedPropertyGroupManager (clase)

Crea grupos de propiedades compartidas y para obtener acceso a los grupos de propiedades compartidos existentes.

Para obtener más información sobre el uso de shared Administrador de propiedades en COM+, vea [COM+ Shared Administrador de propiedades](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Value |
|------------|--------------------------------------------------------------------|
| CLSID      | CLSID \_ SharedPropertyGroupManager                                  |
| ProgID     | L"MTxSpm.SharedPropertyGroupManager"                               |
| Interfaces | [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto SharedPropertyGroupManager se puede declarar mediante "COMSVCSLib.SharedPropertyGroupManager" como nombre de clase.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroup**](sharedpropertygroup.md)
</dt> </dl>

 

 




