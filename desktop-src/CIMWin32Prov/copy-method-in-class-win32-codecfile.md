---
description: Copia el archivo de códec lógico o directorio especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Método Copy de la clase Win32_CodecFile copia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2a7320e4e8474f88ac6721862b50b89534c098db74ac3dc844b50987cb08095d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504955"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a>Método Copy de la clase CodecFile de Win32 \_

El **método copy** wmi [class](/windows/desktop/WmiSdk/retrieving-a-class) copia el archivo de códec lógico o el directorio especificados en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada. No se admite una copia si se requiere sobrescribir un archivo lógico existente.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nombre completo de la copia del archivo (o directorio). Ejemplo: c: \\ temp \\ newdirectory.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el archivo se copió correctamente y cualquier otro número para indicar un error.

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

[**CodecFile de Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

