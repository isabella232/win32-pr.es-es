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
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="029ae-103">CBasePropertyPage. OnReceiveMessage, método</span><span class="sxs-lookup"><span data-stu-id="029ae-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="029ae-104">`OnReceiveMessage`Se llama al método cuando el cuadro de diálogo recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="029ae-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="029ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="029ae-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="029ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="029ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029ae-107">*identificador*</span><span class="sxs-lookup"><span data-stu-id="029ae-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="029ae-108">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="029ae-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="029ae-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="029ae-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="029ae-110">Message.</span><span class="sxs-lookup"><span data-stu-id="029ae-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="029ae-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="029ae-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="029ae-112">Primer parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="029ae-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="029ae-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="029ae-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="029ae-114">Segundo parámetro del mensaje.</span><span class="sxs-lookup"><span data-stu-id="029ae-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029ae-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="029ae-115">Return value</span></span>

<span data-ttu-id="029ae-116">Devuelve un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="029ae-116">Returns a Boolean value.</span></span> <span data-ttu-id="029ae-117">El procedimiento de cuadro de diálogo devuelve este valor; para obtener más información, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="029ae-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="029ae-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="029ae-118">Remarks</span></span>

<span data-ttu-id="029ae-119">La implementación de la clase base llama a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="029ae-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="029ae-120">Invalide este método para controlar los mensajes relacionados con los controles de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="029ae-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="029ae-121">Si el método de reemplazo no controla un mensaje determinado, debe llamar al método de clase base.</span><span class="sxs-lookup"><span data-stu-id="029ae-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="029ae-122">Si el usuario cambia las propiedades a través de los controles de cuadro de diálogo, establezca la marca [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="029ae-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="029ae-123">A continuación, llame al método **IPropertyPageSite:: OnStatusChange** en el puntero [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) para informar del marco.</span><span class="sxs-lookup"><span data-stu-id="029ae-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="029ae-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="029ae-124">Examples</span></span>

<span data-ttu-id="029ae-125">En el siguiente ejemplo se responde a un clic de botón mediante la actualización de una variable miembro, que se supone que se define en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="029ae-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="029ae-126">En este ejemplo también se muestra una función auxiliar para establecer el estado de modificación de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="029ae-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="029ae-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="029ae-127">Requirements</span></span>



| <span data-ttu-id="029ae-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="029ae-128">Requirement</span></span> | <span data-ttu-id="029ae-129">Value</span><span class="sxs-lookup"><span data-stu-id="029ae-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="029ae-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="029ae-130">Header</span></span><br/>  | <dl> <span data-ttu-id="029ae-131"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="029ae-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="029ae-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="029ae-132">Library</span></span><br/> | <dl> <span data-ttu-id="029ae-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="029ae-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029ae-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="029ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029ae-135">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="029ae-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




