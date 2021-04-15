---
description: Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668431"
---
# <a name="cim_owningjobelement-class"></a>\_Clase OwningJobElement de CIM

Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo. Dado que un trabajo puede moverse entre sistemas y el elemento administrado podría no existir durante toda la duración del trabajo, en algunos casos, es posible que esta asociación no sea posible o que solo exista para una parte de la existencia del trabajo.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ OwningJobElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ OwningJobElement** tiene estas propiedades.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ trabajo CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Referencia al trabajo creado por el elemento administrado.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Referencia al elemento administrado que creó el trabajo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

