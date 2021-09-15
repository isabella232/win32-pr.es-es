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
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360628"
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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




