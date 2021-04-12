---
description: Describe las estadísticas de intercambio relacionadas con las llamadas a PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Estructura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280372"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="9b22d-103">Estructura D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="9b22d-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="9b22d-104">Describe las estadísticas de intercambio relacionadas con las llamadas a [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="9b22d-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b22d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b22d-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="9b22d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b22d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9b22d-107">**PresentCount**</span><span class="sxs-lookup"><span data-stu-id="9b22d-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b22d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b22d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b22d-109">Se está ejecutando el recuento de las llamadas presentes correctas realizadas por un dispositivo de pantalla que actualmente se está mostrando en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9b22d-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="9b22d-110">Este parámetro es realmente el identificador actual de la última llamada presente y no es necesariamente el número total de llamadas API presentes realizadas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="9b22d-111">**PresentRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="9b22d-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b22d-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b22d-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b22d-113">El recuento de VBlank en el que se mostró el último presente en la pantalla, el recuento de VBlank se incrementa una vez cada intervalo de VBlank.</span><span class="sxs-lookup"><span data-stu-id="9b22d-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="9b22d-114">**SyncRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="9b22d-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="9b22d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b22d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9b22d-116">El recuento de VBlank cuando el programador muestrea por última vez la hora del equipo mediante una llamada a QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="9b22d-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="9b22d-117">**SyncQPCTime**</span><span class="sxs-lookup"><span data-stu-id="9b22d-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="9b22d-118">Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="9b22d-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="9b22d-119">La última hora del equipo muestreada del programador, obtenida llamando a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="9b22d-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="9b22d-120">**SyncGPUTime**</span><span class="sxs-lookup"><span data-stu-id="9b22d-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="9b22d-121">Tipo: **[ **\_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="9b22d-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="9b22d-122">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9b22d-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b22d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b22d-123">Remarks</span></span>

<span data-ttu-id="9b22d-124">Cuando una aplicación 9Ex adopta el modo de volteo presente (D3DSWAPEFFECT \_ FLIPEX), las aplicaciones pueden detectar la caída de fotogramas llamando a GetPresentStatistics en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="9b22d-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="9b22d-125">En efecto, pueden hacer lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="9b22d-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="9b22d-126">Representar en el búfer de reserva</span><span class="sxs-lookup"><span data-stu-id="9b22d-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="9b22d-127">Llamar a present</span><span class="sxs-lookup"><span data-stu-id="9b22d-127">Call Present</span></span>
3.  <span data-ttu-id="9b22d-128">Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="9b22d-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="9b22d-129">Representar el siguiente fotograma en el búfer de reserva</span><span class="sxs-lookup"><span data-stu-id="9b22d-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="9b22d-130">Llamar a present</span><span class="sxs-lookup"><span data-stu-id="9b22d-130">Call Present</span></span>
6.  <span data-ttu-id="9b22d-131">Repita los pasos 4 y 5 1 o más veces</span><span class="sxs-lookup"><span data-stu-id="9b22d-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="9b22d-132">Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="9b22d-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="9b22d-133">Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="9b22d-134">La aplicación puede calcular el PresentRefreshCount correspondiente de un parámetro PresentCount determinado en función de las suposiciones de PresentRefreshCount incremento y PresentCount de la asignación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="9b22d-135">Si la última muestra de PresentRefreshCount no coincide con el PresentCount (es decir, si el PresentRefreshCount ha aumentado pero PresentCount no, entonces se ha descartado el marco).</span><span class="sxs-lookup"><span data-stu-id="9b22d-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="9b22d-136">Las aplicaciones pueden determinar si un fotograma se ha quitado mediante el muestreo de dos instancias de PresentCount y GetPresentStats (llamando a la API GetPresentStats en dos puntos en el tiempo).</span><span class="sxs-lookup"><span data-stu-id="9b22d-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="9b22d-137">Por ejemplo, una aplicación multimedia que se presenta a la misma velocidad que la frecuencia de actualización del monitor (por ejemplo, la frecuencia de actualización del monitor es 60 Hz, la aplicación presenta un fotograma cada 1/60 segundos) desea presentar los fotogramas a, B, C, D, E, cada uno correspondiente a los identificadores presentes (PresentCount) 1, 2, 3, 7</span><span class="sxs-lookup"><span data-stu-id="9b22d-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="9b22d-138">El código de aplicación tiene un aspecto similar al de la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b22d-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="9b22d-139">Representar el marco a en el búfer de reserva</span><span class="sxs-lookup"><span data-stu-id="9b22d-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="9b22d-140">Call Present, PresentCount = 1</span><span class="sxs-lookup"><span data-stu-id="9b22d-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="9b22d-141">Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="9b22d-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="9b22d-142">Representar los 4 fotogramas siguientes, B, C, D, E, respectivamente</span><span class="sxs-lookup"><span data-stu-id="9b22d-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="9b22d-143">Llamar a present 4 veces, PresentCounts = 2, 3, 7, 8, respectivamente</span><span class="sxs-lookup"><span data-stu-id="9b22d-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="9b22d-144">Llamar a GetPresentStats y almacenar la estructura D3DPRESENTSTATS resultante</span><span class="sxs-lookup"><span data-stu-id="9b22d-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="9b22d-145">Compare los valores de PresentRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="9b22d-146">Si la diferencia es 2, es decir, ha transcurrido 2 intervalos de VBlank entre las dos llamadas a la API de GetPresentStats, el último fotograma presentado debe ser el fotograma C. Dado que la aplicación presenta un intervalo de VBlank (la frecuencia de actualización del monitor), el tiempo transcurrido entre el momento en que se presenta el marco A y el momento en que se presenta el fotograma C debe ser 2 vblanks.</span><span class="sxs-lookup"><span data-stu-id="9b22d-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="9b22d-147">Compare los valores de PresentCount de las dos estructuras D3DPRESENTSTATS almacenadas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="9b22d-148">Si el primer PresentCount es 1 (correspondiente al marco a) y el segundo PresentCount es 3 (correspondiente al marco C), no se ha quitado ningún fotograma.</span><span class="sxs-lookup"><span data-stu-id="9b22d-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="9b22d-149">Si el segundo PresentCount es 3, que corresponde a Frame D, la aplicación sabe que se ha quitado un fotograma.</span><span class="sxs-lookup"><span data-stu-id="9b22d-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="9b22d-150">Tenga en cuenta que GetPresentStatistics se procesará después de llamarse, independientemente del estado de FLIPEX Mode PresentEx calls.</span><span class="sxs-lookup"><span data-stu-id="9b22d-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="9b22d-151">**Windows Vista:** Las llamadas presentes se pondrán en cola y se procesarán antes de que se procese la llamada a GetPresentStats.</span><span class="sxs-lookup"><span data-stu-id="9b22d-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="9b22d-152">Cuando una aplicación detecta que la presentación de determinados fotogramas está detrás, puede omitir esos marcos y corregir la presentación para volver a sincronizar con el VBlank.</span><span class="sxs-lookup"><span data-stu-id="9b22d-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="9b22d-153">Para ello, una aplicación simplemente no puede representar los fotogramas finales y comenzar la representación con el siguiente marco correcto en la cola.</span><span class="sxs-lookup"><span data-stu-id="9b22d-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="9b22d-154">Sin embargo, si una aplicación ya ha iniciado la representación de fotogramas en tiempo de ejecución, puede usar un nuevo parámetro presente en D3D9Ex denominado D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="9b22d-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="9b22d-155">La marca se pasará en los parámetros de la llamada de API presente e indica al tiempo de ejecución que el marco se procesará inmediatamente dentro del intervalo de VBlank siguiente, de modo que no es visible en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9b22d-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="9b22d-156">Este es el ejemplo de uso de la aplicación después del último paso del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="9b22d-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="9b22d-157">Representar el siguiente fotograma en el búfer de reserva</span><span class="sxs-lookup"><span data-stu-id="9b22d-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="9b22d-158">Detectar desde PresentRefreshCount que el siguiente fotograma ya está retrasado</span><span class="sxs-lookup"><span data-stu-id="9b22d-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="9b22d-159">Establecer el intervalo presente en D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="9b22d-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="9b22d-160">Llamada presente en el siguiente fotograma</span><span class="sxs-lookup"><span data-stu-id="9b22d-160">Call Present on the next frame</span></span>

<span data-ttu-id="9b22d-161">Las aplicaciones pueden sincronizar secuencias de audio y vídeo de la misma manera porque el comportamiento de GetPresentStatistics no cambia en ese escenario.</span><span class="sxs-lookup"><span data-stu-id="9b22d-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="9b22d-162">El modo Flip de D3D9Ex proporciona información de estadísticas de fotogramas para aplicaciones en ventanas y aplicaciones 9Ex de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9b22d-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="9b22d-163">**Windows Vista:** Usar las API de DWM para recuperar estadísticas presentes.</span><span class="sxs-lookup"><span data-stu-id="9b22d-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="9b22d-164">Cuando Administrador de ventanas de escritorio está desactivado, las aplicaciones de modo de ventana 9Ex que usan el modo Flip recibirán información de estadísticas presentes de precisión limitada.</span><span class="sxs-lookup"><span data-stu-id="9b22d-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="9b22d-165">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="9b22d-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="9b22d-166">Si una aplicación no es lo suficientemente rápida como para mantenerse al día de la frecuencia de actualización del monitor, probablemente debido a un hardware lento o a la falta de recursos del sistema, puede experimentar un problema con los gráficos.</span><span class="sxs-lookup"><span data-stu-id="9b22d-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="9b22d-167">Un problema es una llamada visual interrupción.</span><span class="sxs-lookup"><span data-stu-id="9b22d-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="9b22d-168">Si un monitor está configurado para actualizar a 60 Hz y la aplicación solo puede administrar 30 fps, la mitad de los fotogramas tendrá problemas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="9b22d-169">Las aplicaciones pueden detectar un problema realizando un seguimiento de SynchRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="9b22d-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="9b22d-170">Por ejemplo, una aplicación puede realizar la siguiente secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="9b22d-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="9b22d-171">Se representa en el búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="9b22d-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="9b22d-172">Llame a Present.</span><span class="sxs-lookup"><span data-stu-id="9b22d-172">Call Present.</span></span>
3.  <span data-ttu-id="9b22d-173">Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.</span><span class="sxs-lookup"><span data-stu-id="9b22d-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="9b22d-174">Representar el siguiente fotograma en el búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="9b22d-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="9b22d-175">Llame a Present.</span><span class="sxs-lookup"><span data-stu-id="9b22d-175">Call Present.</span></span>
6.  <span data-ttu-id="9b22d-176">Llame a GetPresentStats y almacene la estructura D3DPRESENTSTATS resultante.</span><span class="sxs-lookup"><span data-stu-id="9b22d-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="9b22d-177">Compare los valores de SyncRefreshCount de las dos estructuras D3DPRESENTSTATS almacenadas.</span><span class="sxs-lookup"><span data-stu-id="9b22d-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="9b22d-178">Si la diferencia es mayor que uno, se omitirá un fotograma.</span><span class="sxs-lookup"><span data-stu-id="9b22d-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b22d-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b22d-179">Requirements</span></span>



| <span data-ttu-id="9b22d-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b22d-180">Requirement</span></span> | <span data-ttu-id="9b22d-181">Value</span><span class="sxs-lookup"><span data-stu-id="9b22d-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b22d-182">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b22d-182">Header</span></span><br/> | <dl> <span data-ttu-id="9b22d-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b22d-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b22d-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b22d-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b22d-185">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9b22d-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
