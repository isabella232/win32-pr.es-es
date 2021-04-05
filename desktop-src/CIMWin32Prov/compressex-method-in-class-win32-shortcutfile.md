---
description: Comprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método Compress).
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: Método CompressEx de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 512511b690ed6769895e9c4f9922d479d66f847e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998162"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a>Método CompressEx de la \_ clase ShortcutFile de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime el archivo de método abreviado lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**compress**](compress-method-in-class-win32-directory.md) ).

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ enuncia\]
</dt> <dd>

Nombre del archivo o directorio en el que se produjo un error en el método [**CompressEx**](compressex-method-in-class-win32-directory.md) . Este parámetro será **null** si el método se ejecuta correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para [**CompressEx**](compressex-method-in-class-win32-directory.md). El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .

</dd> <dt>

*Recursivo* \[ en, opcional\]
</dt> <dd>

Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .

> [!Note]  
> En el caso de las instancias de archivo, se omite el parámetro *Recursive* .

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.

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

Se produjo un error no especificado.

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

La plataforma no es Windows.

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

Se ha producido una infracción de uso compartido.

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
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

