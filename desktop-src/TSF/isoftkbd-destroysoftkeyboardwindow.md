---
title: Método ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: El método ISoftKbd DestroySoftKeyboardWindow destruye una ventana de teclado en pantalla.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Método DestroySoftKeyboardWindow marco de trabajo de servicios de texto
- Método DestroySoftKeyboardWindow marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685991"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a>ISoftKbd::D método estroySoftKeyboardWindow

El método **ISoftKbd::D estroysoftkeyboardwindow** destruye una ventana de teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                | Descripción                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método quita una ventana de teclado en pantalla creada previamente con una llamada a [**ISoftKbd:: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





