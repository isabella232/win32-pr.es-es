---
title: Método ISoftKbd CreateSoftKeyboardWindow (Softkbdc.h)
description: El método CreateSoftKeyboardWindow de ISoftKbd crea una ventana de teclado flexible.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Método CreateSoftKeyboardWindow Text Services Framework
- Método CreateSoftKeyboardWindow Text Services Framework , interfaz ISoftKbd
- Interfaz ISoftKbd Text Services Framework , método CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953ce70385585349ee905f83e999fb2fc4d71402d2baada413452c729032cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952734"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISoftKbd::CreateSoftKeyboardWindow (método)

El **método ISoftKbd::CreateSoftKeyboardWindow** crea una ventana de teclado flexible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hOwner* \[ En\]
</dt> <dd>

Identificador de la ventana para contener el teclado flexible.

</dd> <dt>

*Tipo de barra \_ de título* \[ en\]
</dt> <dd>

Tipo de barra de título para la ventana de teclado flexible. La enumeración [**TITLEBAR \_ TYPE**](titlebar-type.md) define los tipos posibles.

</dd> <dt>

*xPos* \[ En\]
</dt> <dd>

Posición x de la esquina superior izquierda de la ventana de teclado flexible.

</dd> <dt>

*yPos* \[ En\]
</dt> <dd>

Posición y de la esquina superior izquierda de la ventana de teclado flexible.

</dd> <dt>

*width* \[ En\]
</dt> <dd>

Ancho de la ventana de teclado flexible.

</dd> <dt>

*alto* \[ En\]
</dt> <dd>

Alto de la ventana de teclado flexible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios parámetros no son válidos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd::D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**TITLEBAR \_ TYPE**](titlebar-type.md)
</dt> </dl>

 

 





