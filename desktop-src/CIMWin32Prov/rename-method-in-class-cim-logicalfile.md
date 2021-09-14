---
description: El método Rename cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o se requiere sobrescribir un archivo lógico existente.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Método Rename de la CIM_LogicalFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062665"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a>Método Rename de la clase \_ LogicalFile de CIM

El **método Rename** cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o se requiere sobrescribir un archivo lógico existente.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* \[ En\]
</dt> <dd>

Nombre completo del nuevo archivo (o directorio).

Ejemplo: "c: \\ temp \\newfile.txt"

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Correcto.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

Acceso denegado.

</dd> <dt>

**Error no especificado**
</dt> <dd>

8

Error no especificado.

</dd> <dt>

**Objeto no válido**
</dt> <dd>

9

Objeto no válido.

</dd> <dt>

**El objeto ya existe**
</dt> <dd>

10

El objeto ya existe.

</dd> <dt>

**Sistema de archivos no NTFS**
</dt> <dd>

11

Sistema de archivos no NTFS.

</dd> <dt>

**Plataforma no NT/Windows 2000**
</dt> <dd>

12

Plataforma no Windows.

</dd> <dt>

**La unidad no es la misma**
</dt> <dd>

13

La unidad no es la misma.

</dd> <dt>

**El directorio no está vacío**
</dt> <dd>

14

El directorio no está vacío.

</dd> <dt>

**Infracción de uso compartido**
</dt> <dd>

15

Infracción de uso compartido.

</dd> <dt>

**Archivo de inicio no válido**
</dt> <dd>

16

Archivo de inicio no válido.

</dd> <dt>

**Privilegios no mantenidos**
</dt> <dd>

17

Privilegio no mantenido.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ LogicalFile](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

