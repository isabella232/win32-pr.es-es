---
title: Método ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: El método ISoftKbd EnumSoftKeyboard enumera los posibles teclados de software que admiten el idioma especificado.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Método EnumSoftKeyboard marco de trabajo de servicios de texto
- Método EnumSoftKeyboard marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491891"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>ISoftKbd:: EnumSoftKeyboard (método)

El método **ISoftKbd:: EnumSoftKeyboard** enumera los posibles teclados de software que admiten el idioma especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*langid* \[ de\]
</dt> <dd>

Identificador de idioma.

</dd> <dt>

*lpdwKeyboard* \[ enuncia\]
</dt> <dd>

Puntero a un búfer en el que este método recupera los identificadores de los teclados de software disponibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *langid* no es válido.<br/> |



 

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

 

 





