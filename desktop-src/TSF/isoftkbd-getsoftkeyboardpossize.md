---
title: Método ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardPosSize recupera la posición inicial y el tamaño de un teclado en pantalla.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Método GetSoftKeyboardPosSize marco de trabajo de servicios de texto
- Método GetSoftKeyboardPosSize marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359780"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>ISoftKbd:: GetSoftKeyboardPosSize (método)

El método **ISoftKbd:: GetSoftKeyboardPosSize** recupera la posición inicial y el tamaño de un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStartPoint* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera una estructura de [punto](/previous-versions//dd162805(v=vs.85)) que indica las coordenadas de la posición superior izquierda del teclado en pantalla.

</dd> <dt>

*lpwidth* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera el ancho del teclado en pantalla.

</dd> <dt>

*lpheight* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera el alto del teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno de los parámetros no es válido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

