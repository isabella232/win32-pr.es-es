---
description: La función WiaAddDevice invoca la interfaz de usuario del Asistente para la instalación de escáneres y cámaras. Es equivalente a ejecutar &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; desde el símbolo del sistema.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Función WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809962"
---
# <a name="wiaadddevice-function"></a>WiaAddDevice función)

La función **WiaAddDevice** invoca la interfaz de usuario del Asistente para la instalación de escáneres y cámaras. Es equivalente a ejecutar "rundll32.exe STI \_ci.dll AddDevice" desde el símbolo del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se debe llamar a esta función con credenciales de administrador. Al ejecutarse en control de cuentas de usuario (LUA), el proceso debe elevarse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




