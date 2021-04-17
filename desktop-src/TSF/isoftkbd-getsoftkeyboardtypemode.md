---
title: Método ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: El método ISoftKbd GetSoftKeyboardTypeMode recupera el modo de tipo para un teclado en pantalla.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Método GetSoftKeyboardTypeMode marco de trabajo de servicios de texto
- Método GetSoftKeyboardTypeMode marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421896"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>ISoftKbd:: GetSoftKeyboardTypeMode (método)

El método **ISoftKbd:: GetSoftKeyboardTypeMode** recupera el modo de tipo para un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpTypeMode* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera el modo de tipo. Se definen los valores posibles para la enumeración [**TYPEMODE**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *lpTypeMode* no es válido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TYPEMODE**](typemode.md)
</dt> </dl>

 

 





