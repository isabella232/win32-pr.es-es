---
description: Comprime el archivo de acceso directo lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método Compress).
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: Método CompressEx de la Win32_ShortcutFile clase
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
ms.openlocfilehash: 71302c86cdf1928bdc451a3062c20885bb808dbc60c8c7ede70314b5aa01ba2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505095"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a>Método CompressEx de la clase ShortcutFile de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime el archivo de acceso directo lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del [**método Compress).**](compress-method-in-class-win32-directory.md)

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*StopFileName* \[ out\]
</dt> <dd>

Nombre del archivo o directorio en el que se ha fallado [**el método CompressEx.**](compressex-method-in-class-win32-directory.md) Este parámetro será **NULL si** el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ en, opcional\]
</dt> <dd>

Denomina el archivo o directorio secundario que se usará como punto de partida para [**CompressEx.**](compressex-method-in-class-win32-directory.md) El *parámetro StartFileName* suele ser el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **NULL,** la operación se realiza en el archivo o directorio especificado en la **llamada a ExecMethod.**

</dd> <dt>

*Recursiva* \[ en, opcional\]
</dt> <dd>

Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios dentro del directorio especificado por la instancia de [**\_ LogicalFile de CIM.**](cim-logicalfile.md)

> [!Note]  
> En el caso de las instancias de archivo, se omite el parámetro *Recursive.*

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se comprimió correctamente y cualquier otro número para indicar un error.

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

Ha habido una infracción de uso compartido.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

