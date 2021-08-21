---
description: Se llama al método OnReceiveMessage cuando el cuadro de diálogo recibe un mensaje.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Método CBasePropertyPage.OnReceiveMessage (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833f0f7ab9192d88440afff75a36fee744ac2fe053c6fe99d1940686c452799a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158137"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>CBasePropertyPage.OnReceiveMessage (método)

Se `OnReceiveMessage` llama al método cuando el cuadro de diálogo recibe un mensaje.

## <a name="syntax"></a>Sintaxis


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

Primer parámetro de mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parámetro de mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano. El procedimiento de diálogo devuelve este valor; Para más información, consulte la documentación del SDK de plataforma.

## <a name="remarks"></a>Comentarios

La implementación de clase base llama **a DefWindowProc**. Invalide este método para controlar los mensajes relacionados con los controles de diálogo. Si el método de reemplazo no controla un mensaje determinado, debe llamar al método de clase base.

Si el usuario cambia alguna propiedad a través de los controles de cuadro de diálogo, establezca la marca [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) en **TRUE.** A continuación, llame al método **IPropertyPageSite::OnStatusChange** en el puntero [**CBasePropertyPage::m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) para informar al marco.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se responde a un clic de botón mediante la actualización de una variable miembro, que se supone que se define en la clase derivada. En este ejemplo también se muestra una función auxiliar para establecer el estado de des dirty de la página de propiedades.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Cprop.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePropertyPage (clase)**](cbasepropertypage.md)
</dt> </dl>

 

 




