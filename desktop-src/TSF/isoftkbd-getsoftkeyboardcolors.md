---
title: Método ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardColors recupera el color del teclado blando correspondiente al tipo de color proporcionado.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Método GetSoftKeyboardColors marco de trabajo de servicios de texto
- Método GetSoftKeyboardColors marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "105689598"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>ISoftKbd:: GetSoftKeyboardColors (método)

El método **ISoftKbd:: GetSoftKeyboardColors** recupera el color del teclado blando correspondiente al tipo de color proporcionado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*colorType* \[ de\]
</dt> <dd>

Valor que especifica el tipo de color que se va a recuperar para el teclado en pantalla. Se definen los valores posibles para la enumeración [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*lpColor* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera un valor [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits que especifica un color RGB.

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

[**ISoftKbd::SetSoftKeyboardColors**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**Property**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

