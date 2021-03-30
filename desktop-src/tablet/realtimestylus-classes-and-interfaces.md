---
description: Esta sección contiene información sobre las interfaces y las clases que se usan en el lápiz óptico en tiempo real.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Clases e interfaces de RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910750"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="50c1f-103">Clases e interfaces de RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="50c1f-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="50c1f-104">Esta sección contiene información sobre las interfaces y las clases que se usan en el lápiz óptico en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="50c1f-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="50c1f-105">Las clases e interfaces del lápiz óptico en tiempo real no son compatibles con la automatización.</span><span class="sxs-lookup"><span data-stu-id="50c1f-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="50c1f-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="50c1f-106">In This Section</span></span>



| <span data-ttu-id="50c1f-107">Clase</span><span class="sxs-lookup"><span data-stu-id="50c1f-107">Class</span></span>                                                      | <span data-ttu-id="50c1f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c1f-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50c1f-109">**RealTimeStylus (clase)**</span><span class="sxs-lookup"><span data-stu-id="50c1f-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="50c1f-110">Implementa la interfaz [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="50c1f-111">[**DynamicRenderer (clase)**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="50c1f-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="50c1f-112">Implementa la interfaz de la [**interfaz IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="50c1f-113">**Clase GestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="50c1f-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="50c1f-114">Implementa la interfaz de la [**interfaz IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="50c1f-115">**Clase StrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="50c1f-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="50c1f-116">Implementa la interfaz de la [**interfaz IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="50c1f-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="50c1f-117">Interfaces</span></span>



| <span data-ttu-id="50c1f-118">Interfaz</span><span class="sxs-lookup"><span data-stu-id="50c1f-118">Interface</span></span>                                                                          | <span data-ttu-id="50c1f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c1f-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50c1f-120">**Interfaz IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="50c1f-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="50c1f-121">Expone métodos que permiten controlar la presentación de los datos del lápiz óptico en tiempo real, ya que el objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) controla los datos.</span><span class="sxs-lookup"><span data-stu-id="50c1f-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="50c1f-122">**Interfaz IGestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="50c1f-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="50c1f-123">Expone métodos que permiten reaccionar a los eventos mediante el reconocimiento de los gestos del lápiz óptico y le permite agregar datos a la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="50c1f-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="50c1f-124">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="50c1f-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="50c1f-125">Controla los datos del paquete de lápiz óptico desde un digitalizador en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="50c1f-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="50c1f-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="50c1f-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="50c1f-127">Extiende la interfaz IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="50c1f-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="50c1f-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="50c1f-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="50c1f-129">Extiende la interfaz IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="50c1f-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="50c1f-130">**Interfaz IRealTimeStylusSynchronization**</span><span class="sxs-lookup"><span data-stu-id="50c1f-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="50c1f-131">Sincroniza el acceso al objeto de la [**clase RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="50c1f-132">**Interfaz IStrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="50c1f-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="50c1f-133">Expone métodos que permiten crear trazos mediante programación.</span><span class="sxs-lookup"><span data-stu-id="50c1f-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="50c1f-134">**Interfaz IStylusPlugin**</span><span class="sxs-lookup"><span data-stu-id="50c1f-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="50c1f-135">Expone métodos que permiten recibir notificaciones de eventos y realizar un procesamiento personalizado basado en esos eventos.</span><span class="sxs-lookup"><span data-stu-id="50c1f-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="50c1f-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="50c1f-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="50c1f-137">Representa un complemento asincrónico que se puede Agregar a la colección de complementos asincrónicos de la [**clase RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="50c1f-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="50c1f-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="50c1f-139">Representa un complemento sincrónico que se puede Agregar a la colección de complementos sincrónicos de la [**clase RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="50c1f-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="50c1f-140">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="50c1f-140">Return Values</span></span>

<span data-ttu-id="50c1f-141">Los métodos de la biblioteca COM devuelven los valores **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="50c1f-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="50c1f-142">A menos que se indique lo contrario, los significados de los valores **HRESULT** se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="50c1f-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="50c1f-143">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="50c1f-143">HRESULT value</span></span>                                   | <span data-ttu-id="50c1f-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c1f-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c1f-145">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="50c1f-145">S\_OK</span></span><br/>                                | <span data-ttu-id="50c1f-146">Correcto.</span><span class="sxs-lookup"><span data-stu-id="50c1f-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="50c1f-147">\_puntero E</span><span class="sxs-lookup"><span data-stu-id="50c1f-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="50c1f-148">Al menos un puntero (para un parámetro de entrada o de salida) no es válido.</span><span class="sxs-lookup"><span data-stu-id="50c1f-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="50c1f-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="50c1f-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="50c1f-150">El miembro intentó pasar un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="50c1f-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="50c1f-151">\_excepción de entrada manuscrita \_</span><span class="sxs-lookup"><span data-stu-id="50c1f-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="50c1f-152">Se produjo una excepción.</span><span class="sxs-lookup"><span data-stu-id="50c1f-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="50c1f-153">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="50c1f-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="50c1f-154">El sistema no puede asignar memoria para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="50c1f-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="50c1f-155">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="50c1f-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="50c1f-156">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="50c1f-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="50c1f-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="50c1f-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="50c1f-158">El miembro intentó usar una operación no válida.</span><span class="sxs-lookup"><span data-stu-id="50c1f-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="50c1f-159">TPC \_ E \_ modo no válido \_</span><span class="sxs-lookup"><span data-stu-id="50c1f-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="50c1f-160">El miembro intentó utilizar un modo no válido.</span><span class="sxs-lookup"><span data-stu-id="50c1f-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="50c1f-161">\_ \_ configuración no válida de TPC E \_</span><span class="sxs-lookup"><span data-stu-id="50c1f-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="50c1f-162">El miembro intentó usar una configuración no válida.</span><span class="sxs-lookup"><span data-stu-id="50c1f-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="50c1f-163">\_Descripción de \_ paquetes no válidos de TPC E \_ \_</span><span class="sxs-lookup"><span data-stu-id="50c1f-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="50c1f-164">El miembro intentó usar una descripción de paquete no válida.</span><span class="sxs-lookup"><span data-stu-id="50c1f-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="50c1f-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50c1f-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c1f-166">Referencia de RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="50c1f-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
