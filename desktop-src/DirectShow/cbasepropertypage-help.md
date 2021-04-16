---
description: 'El método de ayuda invoca la ayuda de la página de propiedades. Este método implementa el método IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Método CBasePropertyPage. Help (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671320"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="2f221-104">CBasePropertyPage. Help (método)</span><span class="sxs-lookup"><span data-stu-id="2f221-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="2f221-105">El `Help` método invoca la ayuda de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="2f221-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="2f221-106">Este método implementa el método **IPropertyPage:: help** .</span><span class="sxs-lookup"><span data-stu-id="2f221-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f221-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f221-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="2f221-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f221-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f221-109">*lpszHelpDir*</span><span class="sxs-lookup"><span data-stu-id="2f221-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="2f221-110">Puntero a la cadena bajo la clave **HelpDir** en la información de CLSID de la página de propiedades en el registro.</span><span class="sxs-lookup"><span data-stu-id="2f221-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f221-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f221-111">Return value</span></span>

<span data-ttu-id="2f221-112">Devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2f221-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f221-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f221-113">Remarks</span></span>

<span data-ttu-id="2f221-114">En la clase base, el método siempre devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2f221-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="2f221-115">Cuando se produce un error en el método, el marco llama a **IPropertyPage:: GetPageInfo** para obtener el nombre del archivo de ayuda y el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2f221-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="2f221-116">De forma predeterminada, son **null**.</span><span class="sxs-lookup"><span data-stu-id="2f221-116">By default, these are **NULL**.</span></span> <span data-ttu-id="2f221-117">Para proporcionar ayuda, por lo tanto, la clase derivada puede invalidar el método `Help` o el método [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2f221-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f221-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f221-118">Requirements</span></span>



| <span data-ttu-id="2f221-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f221-119">Requirement</span></span> | <span data-ttu-id="2f221-120">Value</span><span class="sxs-lookup"><span data-stu-id="2f221-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f221-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f221-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2f221-122"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f221-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2f221-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f221-123">Library</span></span><br/> | <dl> <span data-ttu-id="2f221-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f221-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f221-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f221-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f221-126">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="2f221-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




