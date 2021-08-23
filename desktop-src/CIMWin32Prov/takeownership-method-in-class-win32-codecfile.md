---
description: 'Método TakeOwnerShip de la clase Win32_CodecFile: el método de clase WMI TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.'
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la Win32_CodecFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96997b7a29d4a7ca0ad586263bfe7846142963f7ba60e4bdf01a3991e3cfcbff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751695"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a>Método TakeOwnerShip de la clase CodecFile de Win32 \_

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es realmente un directorio, **TakeOwnerShip** actúa de forma recursiva, tomando posesión de todos los archivos y subdirectorios que contiene el directorio.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores enteros.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**CodecFile de Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

