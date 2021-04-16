---
description: Una función de creador estático que puede crear un XamlUIPresenter para una superficie de representación en una aplicación de escritorio.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719022"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="b3b13-103">CreateXamlUIPresenter función)</span><span class="sxs-lookup"><span data-stu-id="b3b13-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="b3b13-104">Una función de creador estático que puede crear un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) para una superficie de representación en una aplicación de escritorio.</span><span class="sxs-lookup"><span data-stu-id="b3b13-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b13-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3b13-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="b3b13-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3b13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3b13-107">*pPresentSite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3b13-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b13-108">Una interfaz de hospedaje existente.</span><span class="sxs-lookup"><span data-stu-id="b3b13-108">An existing hosting interface.</span></span> <span data-ttu-id="b3b13-109">Consulte **IViewObjectPresentNotifySite** en la documentación de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b3b13-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="b3b13-110">*ppPresenter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3b13-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b13-111">La interfaz **\[ \] Exclusive** para un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="b3b13-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3b13-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3b13-112">Return value</span></span>

<span data-ttu-id="b3b13-113">Un **valor HRESULT** estándar, **es \_ correcto** para el éxito.</span><span class="sxs-lookup"><span data-stu-id="b3b13-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b13-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3b13-114">Remarks</span></span>

<span data-ttu-id="b3b13-115">La llamada a este método requiere un **DllImport** de Windows.UI.Xaml.dll.</span><span class="sxs-lookup"><span data-stu-id="b3b13-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="b3b13-116">No se puede llamar a este método desde una aplicación de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="b3b13-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b13-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b13-117">Requirements</span></span>



| <span data-ttu-id="b3b13-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b13-118">Requirement</span></span> | <span data-ttu-id="b3b13-119">Value</span><span class="sxs-lookup"><span data-stu-id="b3b13-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b13-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3b13-120">Header</span></span><br/> | <dl> <span data-ttu-id="b3b13-121"><dt>Windows. UI. Xaml-coretypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3b13-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="b3b13-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3b13-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="b3b13-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3b13-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="b3b13-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3b13-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b13-125">**XamlUIPresenter**</span><span class="sxs-lookup"><span data-stu-id="b3b13-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
