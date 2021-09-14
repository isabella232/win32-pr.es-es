---
description: Descomprime el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Uncompress.
ms.assetid: d4cfa42e-7f05-4d12-b629-14195fc04e77
ms.tgt_platform: multiple
title: Método UncompressEx de la Win32_PageFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 158efe4d2390762433d66d170b774838c9e534d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061491"
---
# <a name="uncompressex-method-of-the-win32_pagefile-class"></a>Método UncompressEx de la clase PageFile de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descomprime el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del [**método Uncompress.**](uncompress-method-in-class-win32-directory.md)

En este tema se Managed Object Format sintaxis de MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nombre del archivo o directorio en el que se ha dado error al método **UncompressEx.** Este parámetro será **NULL si** el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Denomina el archivo o directorio secundario que se usará como punto de partida para **UncompressEx.** El *parámetro StartFileName suele* ser el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **NULL**, la operación se realiza en el archivo o directorio especificado en la llamada a ExecMethod.

</dd> <dt>

*Recursiva* \[ in, opcional\]
</dt> <dd>

Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM.**](cim-logicalfile.md)

> [!Note]  
> En el caso de las instancias de archivo, se omite el parámetro *Recursive.*

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se descomprimió correctamente y cualquier otro número para indicar un error.

<dl> <dt>

**0**
</dt> <dd>

La solicitud fue correcta.

</dd> <dt>

**2**
</dt> <dd>

Se denegó el acceso.

</dd> <dt>

**8**
</dt> <dd>

Error no especificado.

</dd> <dt>

**9**
</dt> <dd>

El nombre especificado no era válido.

</dd> <dt>

**10**
</dt> <dd>

El objeto especificado ya existe.

</dd> <dt>

**11**
</dt> <dd>

El sistema de archivos no es NTFS.

</dd> <dt>

**12**
</dt> <dd>

La plataforma no está Windows.

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

Se ha infringido el uso compartido.

</dd> <dt>

**16**
</dt> <dd>

El archivo de inicio especificado no era válido.

</dd> <dt>

**17**
</dt> <dd>

No se mantiene un privilegio necesario para la operación.

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado no es válido.

</dd> </dl>

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ PageFile**](win32-pagefile.md)
</dt> </dl>

 

