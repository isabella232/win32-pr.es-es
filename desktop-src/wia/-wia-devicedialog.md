---
description: Lo usan las aplicaciones para mostrar un cuadro de diálogo de dispositivo al usuario.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Función DeviceDialog (Wiadevd. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697172"
---
# <a name="devicedialog-function"></a>DeviceDialog función)

Lo usan las aplicaciones para mostrar un cuadro de diálogo de dispositivo al usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeviceDialogData* \[ de\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA**

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) que se va a usar para crear el cuadro de diálogo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




