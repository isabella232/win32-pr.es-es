---
description: La función GetFrame devuelve un identificador a un fotograma determinado dentro de una captura.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Función GetFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169314"
---
# <a name="getframe-function"></a>Función GetFrame

La **función GetFrame** devuelve un identificador a un fotograma determinado dentro de una captura.

## <a name="syntax"></a>Sintaxis


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ En\]
</dt> <dd>

Identificador de una captura. Para obtener el identificador de captura, llame a [la función GetFrameCaptureHandle.](getframecapturehandle.md)

</dd> <dt>

*FrameNumber* \[ En\]
</dt> <dd>

Número (basado en cero) del marco. El número del primer fotograma de una captura es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador para el marco.

Si la función no se realiza correctamente (es decir, si *hCapture* no es válido o el número de fotograma está fuera del intervalo), el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

Use la **función GetFrame** para obtener el identificador de marco necesario al buscar instancias de una propiedad. Las funciones que se usan para buscar instancias de propiedad son [FindPropertyInstance,](findpropertyinstance.md) que busca la primera instancia, y [FindPropertyInstanceRestart,](findpropertyinstancerestart.md) que busca la instancia siguiente.

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetFrame.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




