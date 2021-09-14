---
description: La clase \_ CIM Mount representa una asociación entre un sistema de archivos y un directorio al que está asociado.
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254625"
---
# <a name="cim_mount-class"></a>Cim \_ Mount (clase)

La **clase \_ CIM Mount** representa una asociación entre un sistema de archivos y un directorio al que está asociado.

La semántica de esta relación requiere que el directorio montado esté contenido por un sistema de archivos (a través de la asociación de almacenamiento de archivos) que sea diferente del sistema de archivos al que se hace referencia como dependiente. El sistema de archivos que contiene el directorio puede ser local o remoto. Por ejemplo, un sistema de archivos local en un sistema de equipos Solaris puede montar un directorio desde el sistema de archivos al que se accede a través de la unidad CDROM del equipo (es decir, otro sistema de archivos local). Por otro lado, en un caso "remoto", el directorio se exporta primero por su sistema de archivos, que se hospeda en otro sistema de equipos que actúa, por ejemplo, como un servidor de archivos. Para distinguir los dos montajes, siempre se debe definir una asociación de exportación [**de CIM \_**](cim-export.md) para los directorios montados o a los que se accede de forma remota.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a>Members

La **clase \_ CIM Mount** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM Mount** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Directorio [**CIM \_ que**](cim-directory.md) describe el directorio montado.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ NFS**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Cim [**\_ NFS que**](cim-nfs.md) describe el sistema de archivos en el que se monta el directorio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**CIM \_ El** montaje se deriva de la [**dependencia CIM \_**](cim-dependency.md).

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

