---
description: El \_ método put Owner establece la ventana primaria de la ventana de vídeo; a continuación, la ventana primaria reenvía determinados mensajes a la ventana de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Método CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661144"
---
# <a name="cbasecontrolwindowput_owner-method"></a><span data-ttu-id="5e989-103">CBaseControlWindow. put ( \_ método de propietario)</span><span class="sxs-lookup"><span data-stu-id="5e989-103">CBaseControlWindow.put\_Owner method</span></span>

<span data-ttu-id="5e989-104">El `put_Owner` método establece la ventana primaria de la ventana de vídeo; a continuación, la ventana primaria reenvía determinados mensajes a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e989-104">The `put_Owner` method sets the video window's parent window; the parent window then forwards certain messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e989-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e989-105">Syntax</span></span>


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a><span data-ttu-id="5e989-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e989-107">*Propietario*</span><span class="sxs-lookup"><span data-stu-id="5e989-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="5e989-108">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="5e989-108">Handle to the parent window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e989-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e989-109">Return value</span></span>

<span data-ttu-id="5e989-110">Devuelve NoError.</span><span class="sxs-lookup"><span data-stu-id="5e989-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e989-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e989-111">Remarks</span></span>

<span data-ttu-id="5e989-112">Internamente, este método llama a la función **SetParent** de Microsoft Win32 para establecer el nuevo propietario y establece el estilo de la ventana primaria en WS \_ Child.</span><span class="sxs-lookup"><span data-stu-id="5e989-112">Internally, this method calls the Microsoft Win32 **SetParent** function to set the new owner and sets the parent window's style to WS\_CHILD.</span></span> <span data-ttu-id="5e989-113">A continuación, la ventana primaria reenvía determinados conjuntos de mensajes (en particular, los mensajes del mouse y del teclado) a la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e989-113">The parent window will then forward certain sets of messages (in particular, mouse and keyboard messages) to the video window.</span></span>

<span data-ttu-id="5e989-114">Después de establecer el propietario de la ventana de vídeo, debe establecer el propietario en **null** y el estilo de ventana del propietario en WS \_ OVERLAPPED y WS \_ CLIPCHILDREN antes de liberar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5e989-114">After you set the video window's owner, you must set the owner to **NULL** and the owner's window style to WS\_OVERLAPPED and WS\_CLIPCHILDREN before releasing the filter graph.</span></span> <span data-ttu-id="5e989-115">Cuando se establece el propietario en **null**, este método desactiva el bit de WS secundario de la ventana primaria \_ .</span><span class="sxs-lookup"><span data-stu-id="5e989-115">When you set the owner to **NULL**, this method turns off the parent window's WS\_CHILD bit.</span></span> <span data-ttu-id="5e989-116">Si no establece el propietario en **null**, la ventana primaria seguirá transmitiendo mensajes a la ventana de vídeo y es probable que se produzcan errores cuando se cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e989-116">If you don't set the owner to **NULL**, the parent window will continue to pass messages to the video window and errors will likely occur when the application closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e989-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e989-117">Requirements</span></span>



| <span data-ttu-id="5e989-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e989-118">Requirement</span></span> | <span data-ttu-id="5e989-119">Value</span><span class="sxs-lookup"><span data-stu-id="5e989-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e989-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e989-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5e989-121"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e989-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e989-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e989-122">Library</span></span><br/> | <dl> <span data-ttu-id="5e989-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5e989-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e989-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e989-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e989-125">**Clase CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5e989-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




