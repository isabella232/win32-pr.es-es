---
description: La clase CIM \_ BootServiceAccessBySAP asocia un servicio de arranque y sus puntos de acceso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: CIM_BootServiceAccessBySAP clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78ea24cb3140d50552884887d66fa2607c00b51635ea38af2150295b0c516ef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959094"
---
# <a name="cim_bootserviceaccessbysap-class"></a>Cim \_ BootServiceAccessBySAP (clase)

La **clase CIM \_ BootServiceAccessBySAP** asocia un servicio de arranque y sus puntos de acceso.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ BootServiceAccessBySAP** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ BootServiceAccessBySAP** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BootService**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**servicio de \_ arranque CIM**](cim-bootservice.md) que describe el servicio de arranque.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BootSAP**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

[**\_ BootSAP cim**](cim-bootsap.md) que describe un punto de acceso para el servicio de arranque.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM BootServiceAccessBySAP** se deriva de [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**Servicio \_ CIMAccessBySAP**](cim-serviceaccessbysap.md)
</dt> </dl>

 

