---
description: El método TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es un directorio, este método actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la CIM_LogicalFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062272"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a>Método TakeOwnerShip de la clase \_ LogicalFile de CIM

El **método TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es un directorio, este método actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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

El sistema de archivos no es NTFS.

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

Privilegios no mantenidos.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[CIM \_ LogicalFile](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

