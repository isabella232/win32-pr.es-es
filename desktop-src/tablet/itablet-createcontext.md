---
description: Crea un objeto de contexto que describe el dispositivo de tableta especificado.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet:: CreateContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912902"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="d5c70-103">ITablet:: CreateContext (método)</span><span class="sxs-lookup"><span data-stu-id="d5c70-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="d5c70-104">Crea un objeto de contexto que describe el dispositivo de tableta especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c70-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c70-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c70-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="d5c70-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c70-107">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-108">Ventana a la que se adjuntará el contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d5c70-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-109">*prcInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-110">\[en, único\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-110">\[in, unique\]</span></span>

<span data-ttu-id="d5c70-111">Rectángulo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="d5c70-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-112">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-113">Marcas que establecen opciones de contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d5c70-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-114">*pTCS* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-115">\[en, único\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-115">\[in, unique\]</span></span>

<span data-ttu-id="d5c70-116">Información detallada sobre el contexto de la tableta que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="d5c70-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-117">*CET* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-118">Valor que habilita o deshabilita los mensajes de contexto que se envían a la ventana.</span><span class="sxs-lookup"><span data-stu-id="d5c70-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-119">*ppCtx* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-120">Puntero al nuevo contexto de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d5c70-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-121">*pTcid* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-122">Valor que identifica de forma única la tableta.</span><span class="sxs-lookup"><span data-stu-id="d5c70-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-123">*ppPD* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-124">Puntero a información acerca de los datos contenidos en cada paquete.</span><span class="sxs-lookup"><span data-stu-id="d5c70-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="d5c70-125">*pSink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c70-126">Objeto [**ITabletEventSink**](itableteventsink.md) en el que se enviarán los mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="d5c70-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c70-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c70-127">Return value</span></span>

<span data-ttu-id="d5c70-128">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d5c70-128">This method can return one of these values.</span></span>



| <span data-ttu-id="d5c70-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c70-129">Return code</span></span>                                                                            | <span data-ttu-id="d5c70-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5c70-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d5c70-131"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c70-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="d5c70-132">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d5c70-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="d5c70-133"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="d5c70-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="d5c70-134">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c70-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5c70-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c70-135">Remarks</span></span>

<span data-ttu-id="d5c70-136">Normalmente, una aplicación obtiene los valores predeterminados del [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica los valores para satisfacer sus necesidades y, a continuación, pasa la estructura de configuración modificada al **método ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="d5c70-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="d5c70-137">Debe implementar la [**interfaz ITabletEventSink**](itableteventsink.md) al llamar al **método ITablet:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="d5c70-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="d5c70-138">El parámetro *dwOptions* es un conjunto de marcadores de bits que describen las opciones de contexto.</span><span class="sxs-lookup"><span data-stu-id="d5c70-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="d5c70-139">En la tabla siguiente se describen estas marcas.</span><span class="sxs-lookup"><span data-stu-id="d5c70-139">The following table describes these flags.</span></span>



| <span data-ttu-id="d5c70-140">Nombre de marca</span><span class="sxs-lookup"><span data-stu-id="d5c70-140">Flag Name</span></span>                                | <span data-ttu-id="d5c70-141">Value</span><span class="sxs-lookup"><span data-stu-id="d5c70-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="d5c70-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5c70-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c70-143">\_margen TCXO</span><span class="sxs-lookup"><span data-stu-id="d5c70-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="d5c70-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5c70-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-145">Especifica que el contexto de entrada de la tableta tendrá un margen.</span><span class="sxs-lookup"><span data-stu-id="d5c70-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="d5c70-146">El margen es un área fuera del área de entrada especificada en la que se asignarán los eventos al borde del área de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5c70-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="d5c70-147">Esta característica facilita la entrada de puntos en el borde del contexto.</span><span class="sxs-lookup"><span data-stu-id="d5c70-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="d5c70-148">PREENLACE TCXO \_</span><span class="sxs-lookup"><span data-stu-id="d5c70-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="d5c70-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d5c70-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-150">El PREENLACE obtiene los paquetes antes de los contextos y los postenlaces normales.</span><span class="sxs-lookup"><span data-stu-id="d5c70-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="d5c70-151">Reciben paquetes en el orden en que se crean.</span><span class="sxs-lookup"><span data-stu-id="d5c70-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="d5c70-152">\_Estado de cursor de TCXO \_</span><span class="sxs-lookup"><span data-stu-id="d5c70-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="d5c70-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d5c70-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-154">El TC devolverá los paquetes aunque el cursor esté activo.</span><span class="sxs-lookup"><span data-stu-id="d5c70-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="d5c70-155">De forma predeterminada, un TC solo devolverá los paquetes cuando el cursor esté inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5c70-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="d5c70-156">TCXO \_ sin \_ cursor \_ inactivo</span><span class="sxs-lookup"><span data-stu-id="d5c70-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="d5c70-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d5c70-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-158">El TC no devolverá los paquetes cuando el cursor esté inactivo.</span><span class="sxs-lookup"><span data-stu-id="d5c70-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="d5c70-159">TCXO \_ no \_ integrado</span><span class="sxs-lookup"><span data-stu-id="d5c70-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="d5c70-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c70-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-161">El contexto no estará integrado.</span><span class="sxs-lookup"><span data-stu-id="d5c70-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="d5c70-162">posthook de TCXO \_</span><span class="sxs-lookup"><span data-stu-id="d5c70-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="d5c70-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d5c70-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-164">Los posthooks reciben paquetes después de los contextos de Tablet PC normales, pero antes del contexto del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5c70-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="d5c70-165">Reciben paquetes en el orden inverso a la creación.</span><span class="sxs-lookup"><span data-stu-id="d5c70-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="d5c70-166">TCXO \_ no \_ Mostrar \_ cursor</span><span class="sxs-lookup"><span data-stu-id="d5c70-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="d5c70-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d5c70-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-168">El TC no establecerá la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="d5c70-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="d5c70-169">TCXO \_ no \_ validar \_ ect</span><span class="sxs-lookup"><span data-stu-id="d5c70-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="d5c70-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d5c70-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-171">El TC no validará los GUID que se pasan en los valores de contexto de la tableta con las propiedades compatibles del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5c70-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d5c70-172">TCXO \_ permitir \_ gestos</span><span class="sxs-lookup"><span data-stu-id="d5c70-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="d5c70-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d5c70-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-174">El TC permitirá que se produzca la detección de gestos (de forma predeterminada, solo se permite en contextos del sistema) y el cliente obtendrá \_ los eventos de gestos.</span><span class="sxs-lookup"><span data-stu-id="d5c70-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="d5c70-175">TCXO \_ permitir \_ \_ pulsaciones de comentarios</span><span class="sxs-lookup"><span data-stu-id="d5c70-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="d5c70-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d5c70-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-177">El TC permitirá mostrar los comentarios del lápiz.</span><span class="sxs-lookup"><span data-stu-id="d5c70-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="d5c70-178">De forma predeterminada, solo se permite en contextos del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5c70-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="d5c70-179">TCXO \_ permitir \_ el \_ barril de comentarios</span><span class="sxs-lookup"><span data-stu-id="d5c70-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="d5c70-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d5c70-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="d5c70-181">El TC permitirá mostrar los comentarios del lápiz.</span><span class="sxs-lookup"><span data-stu-id="d5c70-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="d5c70-182">De forma predeterminada, solo se permite en contextos del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5c70-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="d5c70-183">TCXO \_ todo</span><span class="sxs-lookup"><span data-stu-id="d5c70-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="d5c70-184">TCXO \_ margin \| TCXO \_ preenganchat \| TCXO \_ cursor \_ State \| TCXO not \_ \_ cursor \_ Down \| TCXO \_ \_ unintegrated \| TCXO \_ posthook \| TCXO no \_ \_ Show \_ cursor TCXO no \| \_ \_ validar \_ ect</span><span class="sxs-lookup"><span data-stu-id="d5c70-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="d5c70-185">Todas las opciones de contexto de Tablet PC definidas.</span><span class="sxs-lookup"><span data-stu-id="d5c70-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="d5c70-186">\_enlace TCXO</span><span class="sxs-lookup"><span data-stu-id="d5c70-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="d5c70-187">TCXO de \_ PREenlace de \| TCXO \_</span><span class="sxs-lookup"><span data-stu-id="d5c70-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="d5c70-188">Combina la funcionalidad de enlace previo y posterior al enlace.</span><span class="sxs-lookup"><span data-stu-id="d5c70-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="d5c70-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c70-189">Requirements</span></span>



| <span data-ttu-id="d5c70-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c70-190">Requirement</span></span> | <span data-ttu-id="d5c70-191">Value</span><span class="sxs-lookup"><span data-stu-id="d5c70-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c70-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c70-192">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c70-193">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5c70-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d5c70-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c70-194">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c70-195">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d5c70-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d5c70-196">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5c70-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5c70-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5c70-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c70-198">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c70-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c70-199">**Interfaz ITablet**</span><span class="sxs-lookup"><span data-stu-id="d5c70-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="d5c70-200">**\_Enumeración de tipo de habilitación de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="d5c70-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="d5c70-201">**Estructura de configuración de \_ contexto de Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="d5c70-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="d5c70-202">**Estructura de descripción de paquetes \_**</span><span class="sxs-lookup"><span data-stu-id="d5c70-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="d5c70-203">**Interfaz ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="d5c70-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="d5c70-204">**Interfaz ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="d5c70-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




