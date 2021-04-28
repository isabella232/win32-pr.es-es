---
description: 'Constructor CBasePropertyPage.CBasePropertyPage: método constructor.'
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Constructor CBasePropertyPage.CBasePropertyPage (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119953"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="f6479-103">Constructor CBasePropertyPage.CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="f6479-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="f6479-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="f6479-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6479-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6479-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="f6479-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6479-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f6479-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f6479-108">Cadena que contiene el nombre del objeto, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="f6479-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="f6479-109">Para obtener más información, [**vea CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f6479-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6479-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="f6479-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f6479-111">Puntero a la interfaz **IUnknown de agregación.**</span><span class="sxs-lookup"><span data-stu-id="f6479-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="f6479-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="f6479-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="f6479-113">Identificador de recurso para el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f6479-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f6479-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="f6479-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="f6479-115">Identificador de recurso de la cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f6479-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f6479-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6479-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="f6479-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6479-117">Requirements</span></span>



| <span data-ttu-id="f6479-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6479-118">Requirement</span></span> | <span data-ttu-id="f6479-119">Value</span><span class="sxs-lookup"><span data-stu-id="f6479-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6479-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6479-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f6479-121"><dt>Cprop.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6479-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f6479-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6479-122">Library</span></span><br/> | <dl> <span data-ttu-id="f6479-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f6479-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6479-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f6479-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6479-125">**CBasePropertyPage (clase)**</span><span class="sxs-lookup"><span data-stu-id="f6479-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




