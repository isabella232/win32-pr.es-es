---
description: Crea y accede a las propiedades compartidas en un grupo de propiedades compartidas.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Clase SharedPropertyGroup (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361660"
---
# <a name="sharedpropertygroup-class"></a>Clase SharedPropertyGroup

Crea y accede a las propiedades compartidas en un grupo de propiedades compartidas.

Para obtener más información sobre el uso del Administrador de propiedades compartido en COM+, vea [COM+ Shared Administrador de propiedades](com--shared-property-manager.md).

## <a name="when-to-implement"></a>Cuándo implementar

ESTA clase se implementa mediante COM+.



| Requisito | Value |
|------------|------------------------------------------------------|
| Interfaces | [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a>Cuándo se usa

Use esta clase para tener acceso a los métodos [**de ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).

## <a name="remarks"></a>Observaciones

Puede crear un objeto **SharedPropertyGroup** mediante el [**método CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) [**de ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de servicios COM+. Un objeto SharedPropertyGroup se crea mediante una llamada al [**método CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) del [**objeto SharedPropertyGroupManager.**](sharedpropertygroupmanager.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[**SharedProperty**](sharedproperty.md)
</dt> <dt>

[**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




