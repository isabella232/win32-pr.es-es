---
title: Método ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: El método ISoftKbd SelectSoftKeyboard selecciona el teclado en pantalla especificado.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Método SelectSoftKeyboard marco de trabajo de servicios de texto
- Método SelectSoftKeyboard marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534900"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a>ISoftKbd:: SelectSoftKeyboard (método)

El método **ISoftKbd:: SelectSoftKeyboard** selecciona el teclado en pantalla especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwKeyboardId* \[ de\]
</dt> <dd>

Identificador del teclado en pantalla que se va a seleccionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *dwKeyboardId* no es válido.<br/> |



 

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
</dt> </dl>

 

 





