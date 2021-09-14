---
description: Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: WM_IME_COMPOSITION mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254811"
---
# <a name="wm_ime_composition-message"></a>Mensaje COMPOSITION \_ de WM IME \_

Se envía a una aplicación cuando el IME cambia el estado de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Carácter DBCS que representa el cambio más reciente en la cadena de composición.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica cómo ha cambiado la cadena de composición o el carácter. Este parámetro puede ser uno o varios de los valores siguientes. Para obtener más información sobre estos valores, vea [Valores de cadena de composición de IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**GCS \_ COMPATTR**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**GCS \_ COMPCLAUSE**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**GCS \_ COMPREADSTR**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**GCS \_ COMPREADATTR**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**GCS \_ COMPREADCLAUSE**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**GCS \_ COMPSTR**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**CURSORPOS de GCS \_**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**GCS \_ DELTASTART**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**GCS \_ RESULTCLAUSE**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**GCS \_ RESULTREADCLAUSE**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**GCS \_ RESULTREADSTR**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**GCS \_ RESULTSTR**
</dt> </dl>

El *parámetro lParam* también puede tener uno o varios de los valores siguientes.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS \_ INSERTCHAR**</dt> </dl>    | Inserte el *carácter de composición wParam* en el punto de inserción actual. Una aplicación debe mostrar el carácter de composición si procesa este mensaje.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ NOMOVECARET**</dt> </dl> | No mueva la posición del cursor de cursor como resultado del procesamiento del mensaje. Por ejemplo, si un IME especifica una combinación de CS INSERTCHAR y \_ CS NOMOVECARET, la aplicación debe insertar el carácter especificado en la posición del cursor de inserción actual, pero no debe mover el carácter de inserción a la siguiente \_ posición. Un mensaje WM \_ IME \_ COMPOSITION posterior con GCS \_ RESULTSTR reemplazará este carácter.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición. De lo contrario, debería enviar el mensaje a la ventana de IME.

Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje al pasarlo a la ventana predeterminada de IME. La ventana IME procesa este mensaje actualizando su apariencia en función de la marca de cambio especificada. Una aplicación puede llamar a [**ImmGetCompositionString para**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) recuperar el nuevo estado de composición.

Si no se establece ninguno de los valores de GCS, el mensaje indica que se ha cancelado la composición actual y las aplicaciones que dibujan la cadena de composición deben \_ eliminar la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h);</dt> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del Administrador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
