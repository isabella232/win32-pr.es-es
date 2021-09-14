---
description: Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o se requiere sobrescribir un archivo lógico existente.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Método Rename de la CIM_Directory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062667"
---
# <a name="rename-method-of-the-cim_directory-class"></a>Método Rename de la clase Cim \_ Directory

El **método Rename** cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o se requiere sobrescribir un archivo lógico existente.

Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

Nuevo nombre completo del archivo (o directorio).

Ejemplo: "c: \\ temp \\newname.txt"

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**0**
</dt> <dd>

Correcto.

</dd> <dt>

**2**
</dt> <dd>

Acceso denegado.

</dd> <dt>

**8**
</dt> <dd>

Error no especificado.

</dd> <dt>

**9**
</dt> <dd>

Objeto no válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto ya existe.

</dd> <dt>

**11**
</dt> <dd>

Sistema de archivos no NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma no Windows.

</dd> <dt>

**13**
</dt> <dd>

La unidad no es la misma.

</dd> <dt>

**14**
</dt> <dd>

El directorio no está vacío.

</dd> <dt>

**15**
</dt> <dd>

Infracción de uso compartido.

</dd> <dt>

**16**
</dt> <dd>

Archivo de inicio no válido.

</dd> <dt>

**17**
</dt> <dd>

Privilegio no mantenido.

</dd> <dt>

**21**
</dt> <dd>

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

[Directorio \_ CIM](rename-method-in-class-cim-directory.md)
</dt> <dt>

[**Directorio \_ CIM**](cim-directory.md)
</dt> </dl>

 

