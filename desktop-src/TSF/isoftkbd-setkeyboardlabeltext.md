---
title: Método ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: El método ISoftKbd SetKeyboardLabelText establece el texto de la etiqueta del diseño de un teclado en pantalla.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Método SetKeyboardLabelText marco de trabajo de servicios de texto
- Método SetKeyboardLabelText marco de trabajo de servicios de texto, interfaz ISoftKbd
- ISoftKbd interface Text Services Framework, método SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803242"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a>ISoftKbd:: SetKeyboardLabelText (método)

El método **ISoftKbd:: SetKeyboardLabelText** establece el texto de la etiqueta del diseño de un teclado en pantalla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hKl* \[ de\]
</dt> <dd>

Identificador que se usa para recuperar el diseño instalado para el teclado en pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                        | Descripción                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Método realizado correctamente.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *hKl* no es válido.<br/> |



 

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

[**ISoftKbd::SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





