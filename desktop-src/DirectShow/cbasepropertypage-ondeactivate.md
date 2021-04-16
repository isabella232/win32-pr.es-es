---
description: Se llama al método OnDeactivate cuando se destruye la ventana del cuadro de diálogo.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Método CBasePropertyPage. OnDeactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671691"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="a58d0-103">CBasePropertyPage. OnDeactivate (método)</span><span class="sxs-lookup"><span data-stu-id="a58d0-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="a58d0-104">`OnDeactivate`Se llama al método cuando se destruye la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a58d0-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a58d0-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="a58d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a58d0-106">Parameters</span></span>

<span data-ttu-id="a58d0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a58d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a58d0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a58d0-108">Return value</span></span>

<span data-ttu-id="a58d0-109">La implementación de la clase base devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a58d0-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a58d0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a58d0-110">Remarks</span></span>

<span data-ttu-id="a58d0-111">El método [**CBasePropertyPage::D eactivate**](cbasepropertypage-deactivate.md) llama al `OnDeactivate` método.</span><span class="sxs-lookup"><span data-stu-id="a58d0-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="a58d0-112">Invalide `OnDeactivate` para liberar los recursos que la clase derivada obtuvo en el método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , o para realizar otras tareas según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a58d0-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a58d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a58d0-113">Requirements</span></span>



| <span data-ttu-id="a58d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a58d0-114">Requirement</span></span> | <span data-ttu-id="a58d0-115">Value</span><span class="sxs-lookup"><span data-stu-id="a58d0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a58d0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a58d0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a58d0-117"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a58d0-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a58d0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a58d0-118">Library</span></span><br/> | <dl> <span data-ttu-id="a58d0-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a58d0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a58d0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a58d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a58d0-121">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="a58d0-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




