---
description: La \_ Asociación ActsAsSpare de CIM indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados. Una reserva puede funcionar en &\# 0034; modo de espera activa&\# 0034; tal y como se especifica en cada elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000699"
---
# <a name="cim_actsasspare-class"></a>\_Clase ActsAsSpare de CIM

La **Asociación \_ ActsAsSpare de CIM** indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados. Una reserva puede funcionar en modo de "espera activa" como se especifica en cada elemento.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ActsAsSpare** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ActsAsSpare** tiene estas propiedades.

<dl> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SpareGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la propiedad de **Grupo** que representa la clase [**\_ SpareGroup de CIM**](cim-sparegroup.md) .

</dd> <dt>

**HotStandby**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, la reserva funciona como una espera activa.

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ManagedSystemElement de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un elemento del sistema administrado que actúa como repuesto y que participa en el grupo de reserva.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

