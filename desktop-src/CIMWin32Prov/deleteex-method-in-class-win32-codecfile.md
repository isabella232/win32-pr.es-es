---
description: Elimine el archivo lógico de códec de audio o vídeo (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Método DeleteEx de la Win32_CodecFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061529"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a>Método DeleteEx de la clase \_ CodecFile win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** eliminará el archivo lógico de códec de audio o vídeo (o directorio) especificado en la ruta de acceso del objeto. **DeleteEx** es una versión extendida del [**método Delete.**](delete-method-in-class-win32-directory.md)

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nombre del archivo o directorio en el que se ha fallado **el método DeleteEx.** Este parámetro será **NULL si** el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ En\]
</dt> <dd>

Denomina el archivo o directorio secundario que se usará como punto de partida para **DeleteEx.** El *parámetro StartFileName* suele ser el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **NULL,** la operación se realiza en el archivo o directorio especificado en la **llamada a ExecMethod.** Este parámetro es opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**CodecFile de Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

