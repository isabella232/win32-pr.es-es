---
description: La \_ clase CIM ServiceServiceDependency representa una asociación entre dos servicios.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: CIM_ServiceServiceDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659510"
---
# <a name="cim_serviceservicedependency-class"></a>\_Clase ServiceServiceDependency de CIM

La clase **CIM \_ ServiceServiceDependency** representa una asociación entre dos servicios. El servicio asociado debe estar presente, debe haberse completado o debe estar ausente para que el otro servicio funcione. Por ejemplo, los servicios de arranque pueden depender del BIOS, el disco y los servicios de inicialización subyacentes. En el caso de los servicios de inicialización, el servicio de arranque depende de la finalización de los servicios de inicialización. En el caso de los servicios de disco, los servicios de arranque pueden utilizar realmente los SAP de este servicio. Esta dependencia de uso se modela en la [**Asociación \_ ServiceSAPDependency de CIM**](cim-servicesapdependency.md) .

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ServiceServiceDependency** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ServiceServiceDependency** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servicio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ servicio CIM**](cim-service.md) que describe el servicio requerido.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ servicio CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

[**\_ Servicio CIM**](cim-service.md) que describe el servicio que depende de un servicio subyacente.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Naturaleza de la dependencia entre servicios. Esta propiedad indica que el servicio asociado debe haber finalizado, debe iniciarse o no debe iniciarse para que el servicio funcione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>El **servicio debe haberse completado** (2)


</dt> <dd>

El servicio debe haberse completado.

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>El **servicio debe iniciarse** (3)


</dt> <dd>

Debe iniciarse el servicio.

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**No se debe iniciar el servicio** (4)


</dt> <dd>

No se debe iniciar el servicio.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ ServiceServiceDependency**, vea [clases Win32](win32-provider.md).

La clase **CIM \_ ServiceServiceDependency** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

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

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

