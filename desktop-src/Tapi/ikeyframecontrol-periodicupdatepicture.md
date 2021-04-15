---
description: Una aplicación llama al método PeriodicUpdatePicture para configurar un temporizador en la secuencia que pedirá actualizaciones de la imagen periódicamente. Las actualizaciones de imágenes causan un uso elevado de ancho de banda, por lo que este método se utilizará normalmente en lugar de UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: IKeyFrameControl::P método eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690007"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a><span data-ttu-id="bfc9f-104">IKeyFrameControl::P método eriodicUpdatePicture</span><span class="sxs-lookup"><span data-stu-id="bfc9f-104">IKeyFrameControl::PeriodicUpdatePicture method</span></span>

<span data-ttu-id="bfc9f-105">\[**PeriodicUpdatePicture** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-105">\[**PeriodicUpdatePicture** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bfc9f-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="bfc9f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bfc9f-107">Una aplicación llama al método **PeriodicUpdatePicture** para configurar un temporizador en la secuencia que pedirá actualizaciones de la imagen periódicamente.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-107">The **PeriodicUpdatePicture** method is called by an application to configure a timer in the stream that will ask for picture updates periodically.</span></span> <span data-ttu-id="bfc9f-108">Las actualizaciones de imágenes causan un uso elevado de ancho de banda, por lo que este método se utilizará normalmente en lugar de [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span><span class="sxs-lookup"><span data-stu-id="bfc9f-108">Picture updates cause high bandwidth usage, so this method will normally be used instead of [**UpdatePicture**](ikeyframecontrol-updatepicture.md).</span></span>

<span data-ttu-id="bfc9f-109">Si se llama al método cuando la secuencia está activa, el temporizador se iniciará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-109">If the method is called when the stream is active, the timer will start immediately.</span></span> <span data-ttu-id="bfc9f-110">Si la secuencia no está activa, el temporizador se iniciará cuando la secuencia entre en el estado activo.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-110">If the stream is not active, the timer will be started when the stream enters the active state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc9f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfc9f-111">Syntax</span></span>


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a><span data-ttu-id="bfc9f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfc9f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfc9f-113">*fEnable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfc9f-113">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc9f-114">**True** habilita el temporizador.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-114">**TRUE** enables the timer.</span></span> <span data-ttu-id="bfc9f-115">**False** lo deshabilita.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-115">**FALSE** disables it.</span></span>

</dd> <dt>

<span data-ttu-id="bfc9f-116">*dwInterval* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfc9f-116">*dwInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfc9f-117">El intervalo del temporizador, en segundos.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-117">The interval for the timer, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfc9f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfc9f-118">Return value</span></span>

<span data-ttu-id="bfc9f-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-119">This method can return one of these values.</span></span>



| <span data-ttu-id="bfc9f-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bfc9f-120">Return code</span></span>                                                                            | <span data-ttu-id="bfc9f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfc9f-121">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bfc9f-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc9f-122"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bfc9f-123">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-123">Method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="bfc9f-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="bfc9f-124"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bfc9f-125">No se pudo realizar por motivos inesperados.</span><span class="sxs-lookup"><span data-stu-id="bfc9f-125">Failed for unexpected reasons.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bfc9f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc9f-126">Requirements</span></span>



| <span data-ttu-id="bfc9f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc9f-127">Requirement</span></span> | <span data-ttu-id="bfc9f-128">Value</span><span class="sxs-lookup"><span data-stu-id="bfc9f-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc9f-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="bfc9f-129">TAPI version</span></span><br/> | <span data-ttu-id="bfc9f-130">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bfc9f-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bfc9f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfc9f-131">Header</span></span><br/>       | <dl> <span data-ttu-id="bfc9f-132"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc9f-132"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="bfc9f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfc9f-133">Library</span></span><br/>      | <dl> <span data-ttu-id="bfc9f-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfc9f-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bfc9f-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfc9f-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="bfc9f-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfc9f-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bfc9f-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfc9f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc9f-138">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="bfc9f-138">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

 




