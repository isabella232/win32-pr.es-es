---
title: Método ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: El método ISoftKbd CreateSoftKeyboardWindow crea una ventana de teclado en pantalla.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Método CreateSoftKeyboardWindow marco de trabajo de servicios de texto
- Método CreateSoftKeyboardWindow marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método CreateSoftKeyboardWindow
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
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534792"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISoftKbd:: CreateSoftKeyboardWindow (método)

El método **ISoftKbd:: CreateSoftKeyboardWindow** crea una ventana de teclado en pantalla.

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

*hOwner* \[ de\]
</dt> <dd>

Identificador de la ventana que va a contener el teclado en pantalla.

</dd> <dt>

*\_ Tipo de TitleBar* \[ en\]
</dt> <dd>

Tipo de barra de título de la ventana de teclado en pantalla. Los tipos posibles se definen mediante la enumeración de [**\_ tipo TITLEBAR**](titlebar-type.md) .

</dd> <dt>

*xPos* \[ de\]
</dt> <dd>

Posición x de la esquina superior izquierda de la ventana de teclado en pantalla.

</dd> <dt>

*yPos* \[ de\]
</dt> <dd>

Posición y de la esquina superior izquierda de la ventana de teclado en pantalla.

</dd> <dt>

*ancho* \[ de de\]
</dt> <dd>

Ancho de la ventana de teclado en pantalla.

</dd> <dt>

*alto* \[ de de\]
</dt> <dd>

Alto de la ventana de teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o más parámetros no son válidos.<br/> |



 

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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd::D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**tipo de TITLEBAR \_**](titlebar-type.md)
</dt> </dl>

 

 





