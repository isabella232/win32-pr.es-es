---
description: Sin comprimir el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de \_ LOGICALFILE CIM.
ms.assetid: a9b5e9bc-1c31-4518-ade4-8e9a0106608e
ms.tgt_platform: multiple
title: Método UNCOMPRESS de la clase CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bc7bd0a9759a3eb02d1faee6b6fb669cde4dba8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274885"
---
# <a name="uncompress-method-of-the-cim_devicefile-class"></a>Método UNCOMPRESS de la \_ clase DeviceFile de CIM

El método **UNCOMPRESS** descomprimió el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Uncompress();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

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

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

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

[\_DEVICEFILE CIM](uncompress-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> </dl>

 

