---
description: Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: Función DvdLauncher
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164374"
---
# <a name="dvdlauncher-function"></a>Función DvdLauncher

Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HWnd* \[ En\]
</dt> <dd>

Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.

</dd> <dt>

*DriveLetter* \[ En\]
</dt> <dd>

Letra de unidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente y las regiones coinciden, el valor devuelto es distinto de cero. De lo contrario, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a StorProp.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administración de dispositivos functions](device-management-functions.md)
</dt> </dl>

 

