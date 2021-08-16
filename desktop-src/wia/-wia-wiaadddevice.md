---
description: La función WiaAddDevice invoca la interfaz de usuario del Asistente para instalación de escáneres y cámaras. Es equivalente a ejecutar &\# 0034;rundll32.execi.dll \_ AddDevice&0034; desde el símbolo del \# sistema.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Función WiaAddDevice (Wia.h)
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
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965404"
---
# <a name="wiaadddevice-function"></a>Función WiaAddDevice

La **función WiaAddDevice** invoca la interfaz de usuario del Asistente para instalación de escáneres y cámaras. Equivale a ejecutar "rundll32.exe de \_ci.dll AddDevice" desde el símbolo del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se debe llamar a esta función con credenciales de administrador. Cuando se ejecuta en Control de cuentas de usuario (LUA), el proceso debe tener privilegios elevados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




