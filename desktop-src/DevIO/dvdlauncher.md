---
description: Comprueba que la región de medios de la unidad de DVD coincide con la región de la unidad de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher función)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153333"
---
# <a name="dvdlauncher-function"></a>DvdLauncher función)

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

*HWnd* \[ de\]
</dt> <dd>

Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.

</dd> <dt>

*LetraDeUnidad* \[ de\]
</dt> <dd>

Letra de la unidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente y las regiones coinciden, el valor devuelto es distinto de cero. De lo contrario, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a StorProp.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de administración de dispositivos](device-management-functions.md)
</dt> </dl>

 

