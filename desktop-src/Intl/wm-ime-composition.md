---
description: Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Mensaje de WM_IME_COMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003138"
---
# <a name="wm_ime_composition-message"></a>Mensaje de composición de \_ IME de WM \_

Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Carácter DBCS que representa el cambio más reciente en la cadena de composición.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica cómo cambió el carácter o la cadena de composición. Este parámetro puede ser uno o varios de los valores siguientes. Para obtener más información sobre estos valores, vea [valores de cadena de composición de IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**GC \_ COMPATTR**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**GC \_ COMPCLAUSE**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**GC \_ COMPREADSTR**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**GC \_ COMPREADATTR**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**GC \_ COMPREADCLAUSE**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**GC \_ COMPSTR**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**GC \_ CURSORPOS**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**GC \_ DELTASTART**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**GC \_ RESULTCLAUSE**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**GC \_ RESULTREADCLAUSE**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**GC \_ RESULTREADSTR**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**RESULTSTR de GC \_**
</dt> </dl>

El parámetro *lParam* también puede tener uno o varios de los valores siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**\_INSERTCHAR CS**</dt> </dl>    | Inserte el carácter de composición *wParam* en el punto de inserción actual. Una aplicación debe mostrar el carácter de composición si procesa este mensaje.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**\_NOMOVECARET CS**</dt> </dl> | No mover la posición del símbolo de intercalación como resultado del procesamiento del mensaje. Por ejemplo, si un IME especifica una combinación de CS \_ INSERTCHAR y CS \_ NOMOVECARET, la aplicación debe insertar el carácter especificado en la posición actual del símbolo de intercalación, pero no debe mover el símbolo de intercalación a la posición siguiente. Un mensaje de \_ composición del IME de WM posterior \_ con RESULTSTR de GC \_ reemplazará este carácter.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición. De lo contrario, debe enviar el mensaje a la ventana del IME.

Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasándolo a la ventana IME predeterminada. La ventana del IME procesa este mensaje actualizando su apariencia en función de la marca de cambio especificada. Una aplicación puede llamar a [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) para recuperar el nuevo estado de composición.

Si no se establece ninguno de los valores de GC \_ , el mensaje indica que se ha cancelado la composición actual y que las aplicaciones que dibujan la cadena de composición deben eliminar la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
