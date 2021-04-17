---
description: Se llama al método OnActivate cuando se activa la página de propiedades.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Método CBasePropertyPage. OnActivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660764"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="23f60-103">CBasePropertyPage. OnActivate (método)</span><span class="sxs-lookup"><span data-stu-id="23f60-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="23f60-104">`OnActivate`Se llama al método cuando se activa la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="23f60-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23f60-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="23f60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23f60-106">Parameters</span></span>

<span data-ttu-id="23f60-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="23f60-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23f60-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23f60-108">Return value</span></span>

<span data-ttu-id="23f60-109">La implementación de la clase base devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="23f60-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f60-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23f60-110">Remarks</span></span>

<span data-ttu-id="23f60-111">El método [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) llama al `OnActivate` método.</span><span class="sxs-lookup"><span data-stu-id="23f60-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="23f60-112">En la clase derivada, invalide `OnActivate` para inicializar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="23f60-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="23f60-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="23f60-113">Examples</span></span>

<span data-ttu-id="23f60-114">En el ejemplo siguiente se inicializa un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="23f60-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="23f60-115">En este ejemplo se da por supuesto que **m \_ pOwningFilter** es un puntero a una interfaz personalizada en el filtro asociado a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="23f60-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="23f60-116">(Use el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) para inicializar estos punteros).</span><span class="sxs-lookup"><span data-stu-id="23f60-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="23f60-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f60-117">Requirements</span></span>



| <span data-ttu-id="23f60-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f60-118">Requirement</span></span> | <span data-ttu-id="23f60-119">Value</span><span class="sxs-lookup"><span data-stu-id="23f60-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f60-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23f60-120">Header</span></span><br/>  | <dl> <span data-ttu-id="23f60-121"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23f60-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="23f60-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23f60-122">Library</span></span><br/> | <dl> <span data-ttu-id="23f60-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="23f60-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f60-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="23f60-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f60-125">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="23f60-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




