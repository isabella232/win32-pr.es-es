---
description: La clase WMI de \_ asociación PnPAllocatedResource de Win32 representa una asociación entre dispositivos lógicos y recursos del sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 492bd510965499393b399e8e02c1b901fc33f9abc00acf191899c5bb6b8b6d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008949"
---
# <a name="win32_pnpallocatedresource-class"></a>Clase \_ PnPAllocatedResource de Win32

La clase WMI **de \_ asociación PnPAllocatedResource** [de](../wmisdk/retrieving-a-class.md) Win32 representa una asociación entre dispositivos lógicos y recursos del sistema. Esta clase se usa para detectar los recursos que un dispositivo específico está utilizando, como un canal de interrupción de la requestación (IRQ) o de acceso directo a memoria (DMA).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ PnPAllocatedResource de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PnPAllocatedResource de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SystemResource**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ SystemResource")
</dt> </dl>

Referencia a la [**instancia \_ systemResource de CIM**](cim-systemresource.md) que representa las propiedades de un recurso del sistema disponible para el dispositivo lógico. Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM \_ LogicalDevice")
</dt> </dl>

Referencia a la [**instancia de Win32 \_ PnPEntity**](win32-pnpentity.md) que representa las propiedades del dispositivo lógico mediante los recursos del sistema asignados a él. Esta propiedad se hereda de la [**dependencia \_ CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PnPAllocatedResource de Win32** se deriva de [**CIM \_ AllocatedResource**](cim-allocatedresource.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
