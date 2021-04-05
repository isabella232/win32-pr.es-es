---
description: La \_ Asociación ElementConfiguration de CIM relaciona un objeto de \_ configuración de CIM con uno o más elementos del sistema administrados. El objeto de configuración de CIM \_ representa un comportamiento determinado o un estado funcional deseado para el ManagedSystemElement de CIM asociado \_ .
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080216"
---
# <a name="cim_elementconfiguration-class"></a>\_Clase ElementConfiguration de CIM

La **Asociación \_ ElementConfiguration de CIM** relaciona un objeto de [**\_ configuración de CIM**](cim-configuration.md) con uno o más elementos del sistema administrados. El objeto de **\_ configuración de CIM** representa un comportamiento determinado o un estado funcional deseado para el [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md)asociado.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ElementConfiguration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ElementConfiguration** tiene estas propiedades.

<dl> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ configuración de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al objeto [**de \_ configuración de CIM**](cim-configuration.md) que agrupa la configuración y las dependencias asociadas al elemento de sistema administrado.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ManagedSystemElement de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al elemento del sistema administrado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




