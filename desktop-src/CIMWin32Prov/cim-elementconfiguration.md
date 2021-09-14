---
description: La \_ asociación ElementConfiguration de CIM relaciona un objeto de configuración de CIM \_ con uno o varios elementos del sistema administrados. El objeto \_ de configuración cim representa un comportamiento determinado o un estado funcional deseado para el elemento \_ ManagedSystemElement de CIM asociado.
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974189"
---
# <a name="cim_elementconfiguration-class"></a>Cim \_ ElementConfiguration (clase)

La **\_ asociación ElementConfiguration** de CIM relaciona un [**objeto de configuración \_ de CIM**](cim-configuration.md) con uno o varios elementos del sistema administrados. El **objeto \_ de configuración** cim representa un comportamiento determinado o un estado funcional deseado para el elemento [**\_ ManagedSystemElement de CIM asociado.**](cim-managedsystemelement.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

## <a name="members"></a>Members

La **clase \_ ElementConfiguration** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ElementConfiguration** de CIM tiene estas propiedades.

<dl> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Configuración de CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al objeto [**de \_ configuración cim**](cim-configuration.md) que agrupa la configuración y las dependencias asociadas al elemento del sistema administrado.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al elemento del sistema administrado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




