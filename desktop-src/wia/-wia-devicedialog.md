---
description: Lo usan las aplicaciones para mostrar un cuadro de diálogo de dispositivo al usuario.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Función DeviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: de8a3d36472d51c24a2c007ad7be0be371a0b5d8bb39e75f457e204250e8f53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441683"
---
# <a name="devicedialog-function"></a>Función DeviceDialog

Lo usan las aplicaciones para mostrar un cuadro de diálogo de dispositivo al usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ En\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA**

[**DEVICEDIALOGDATA que se**](-wia-devicedialogdata.md) usará para crear el cuadro de diálogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




