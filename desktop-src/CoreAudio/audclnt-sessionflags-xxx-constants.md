---
description: Las \_ \_ constantes de AUDCLNT SESSIONFLAGS XXX indican características de una sesión de audio asociada a la secuencia.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes de AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496696"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="c2ead-103">Constantes de AUDCLNT \_ SESSIONFLAGS \_ XXX</span><span class="sxs-lookup"><span data-stu-id="c2ead-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="c2ead-104">Las \_ \_ constantes de AUDCLNT SESSIONFLAGS XXX indican características de una sesión de audio asociada a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c2ead-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="c2ead-105">Un cliente puede especificar estas opciones durante la inicialización de la secuencia mediante el parámetro *StreamFlags* del método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="c2ead-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="c2ead-106">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="c2ead-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c2ead-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2ead-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="c2ead-108"><dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="c2ead-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="c2ead-109">La sesión expira cuando no hay secuencias asociadas y objetos de control de sesión propietarios que contienen referencias.</span><span class="sxs-lookup"><span data-stu-id="c2ead-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="c2ead-110"><dt>**AUDCLNT \_ SESSIONFLAGS \_ Mostrar \_ ocultar**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="c2ead-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="c2ead-111">El control de volumen se oculta en la interfaz de usuario del mezclador de volumen cuando se crea la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="c2ead-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="c2ead-112">Si la sesión asociada a la secuencia ya existe antes de que [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Abra el flujo, el control de volumen se mostrará en el mezclador de volumen.</span><span class="sxs-lookup"><span data-stu-id="c2ead-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="c2ead-113"><dt> **AUDCLNT \_ SESSIONFLAGS \_ Display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="c2ead-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="c2ead-114">El control de volumen se oculta en la interfaz de usuario del mezclador de volumen después de que expire la sesión.</span><span class="sxs-lookup"><span data-stu-id="c2ead-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="c2ead-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2ead-115">Requirements</span></span>



| <span data-ttu-id="c2ead-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2ead-116">Requirement</span></span> | <span data-ttu-id="c2ead-117">Value</span><span class="sxs-lookup"><span data-stu-id="c2ead-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ead-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2ead-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ead-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2ead-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2ead-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2ead-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ead-121">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2ead-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2ead-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2ead-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ead-123"><dt>Audiosessiontypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ead-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ead-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2ead-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ead-125">Constantes de audio principales</span><span class="sxs-lookup"><span data-stu-id="c2ead-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="c2ead-126">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="c2ead-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




