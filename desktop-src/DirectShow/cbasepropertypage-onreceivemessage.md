---
description: Se llama al método OnReceiveMessage cuando el cuadro de diálogo recibe un mensaje.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Método CBasePropertyPage. OnReceiveMessage (Cprop. h)
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
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670509"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>CBasePropertyPage. OnReceiveMessage, método

`OnReceiveMessage`Se llama al método cuando el cuadro de diálogo recibe un mensaje.

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

*identificador* 
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

Segundo parámetro del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano. El procedimiento de cuadro de diálogo devuelve este valor; para obtener más información, consulte la documentación del SDK de la plataforma.

## <a name="remarks"></a>Observaciones

La implementación de la clase base llama a **DefWindowProc**. Invalide este método para controlar los mensajes relacionados con los controles de cuadro de diálogo. Si el método de reemplazo no controla un mensaje determinado, debe llamar al método de clase base.

Si el usuario cambia las propiedades a través de los controles de cuadro de diálogo, establezca la marca [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) en **true**. A continuación, llame al método **IPropertyPageSite:: OnStatusChange** en el puntero [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) para informar del marco.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se responde a un clic de botón mediante la actualización de una variable miembro, que se supone que se define en la clase derivada. En este ejemplo también se muestra una función auxiliar para establecer el estado de modificación de la página de propiedades.


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
| Encabezado<br/>  | <dl> <dt>Cprop. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




