---
description: Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: CIM_OwningJobElement clase
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
ms.openlocfilehash: 8ea0e4371246f71d125295730c19de75c59eafb08a4c081699b6b40575f27a99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694665"
---
# <a name="cim_owningjobelement-class"></a>Cim \_ OwningJobElement (clase)

Representa una asociación entre un trabajo y el elemento administrado que creó el trabajo. Dado que un trabajo puede moverse entre sistemas y es posible que el elemento administrado no exista durante toda la duración del trabajo, en algunos casos, es posible que esta asociación no sea posible o solo exista para una parte de la existencia del trabajo.

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

La **clase CIM \_ OwningJobElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ OwningJobElement** tiene estas propiedades.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **Trabajo CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Referencia al trabajo creado por el elemento administrado.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia al elemento administrado que creó el trabajo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

