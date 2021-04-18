---
description: Información general sobre el modelo en cascada para la clase RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: El modelo RealTimeStylus en cascada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564225"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="dbba8-103">El modelo RealTimeStylus en cascada</span><span class="sxs-lookup"><span data-stu-id="dbba8-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="dbba8-104">El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada permite usar dos objetos **RealTimeStylus** , cada uno de los cuales se ejecuta en un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="dbba8-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="dbba8-105">Con este modelo, se adjunta un objeto **RealTimeStylus** secundario a un objeto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="dbba8-106">El objeto **RealTimeStylus** secundario se adjunta como el único complemento asincrónico en la colección de complementos asincrónica del objeto **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="dbba8-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="dbba8-107">El modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada puede ser útil en los escenarios siguientes.</span><span class="sxs-lookup"><span data-stu-id="dbba8-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="dbba8-108">Puede Agregar a la colección de complementos sincrónicos del objeto [**RealTimeStylus**](realtimestylus-class.md) el acceso en tiempo real al flujo de datos del lápiz de Tablet PC, como el reconocimiento de gestos de varios trazos.</span><span class="sxs-lookup"><span data-stu-id="dbba8-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="dbba8-109">Puede distribuir la carga de cálculo de los complementos sincrónicos en dos subprocesos, lo que reduce los retrasos en la recopilación de entradas manuscritas en algunos Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dbba8-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="dbba8-110">En el diagrama siguiente se ilustra el flujo de datos del lápiz de Tablet PC a través de dos objetos [**RealTimeStylus**](realtimestylus-class.md) en cascada y sus colecciones de complementos.</span><span class="sxs-lookup"><span data-stu-id="dbba8-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![Ilustración que muestra el flujo de datos RealTimeStylus en cascada](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="dbba8-112">En este diagrama, la letra "A" del círculo representa los datos del lápiz de Tablet PC que ya han sido procesados por los objetos [**RealTimeStylus**](realtimestylus-class.md) principal y secundario, y se han colocado en la cola de salida del objeto **RealTimeStylus** secundario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="dbba8-113">La letra "B" en el círculo representa los datos del lápiz de Tablet PC que ya ha procesado el objeto **RealTimeStylus** principal y se han agregado a la cola de salida del objeto **RealTimeStylus** principal y aún no se ha enviado al objeto **RealTimeStylus** secundario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="dbba8-114">La letra "C" de círculo representa los datos del lápiz de Tablet PC que está procesando actualmente el objeto **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="dbba8-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="dbba8-115">Se envía a la colección de complementos sincrónicos y se coloca en la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="dbba8-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="dbba8-116">El círculo vacío representa la posición en la cola de salida donde se agregan los datos futuros del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="dbba8-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="dbba8-117">Restricciones</span><span class="sxs-lookup"><span data-stu-id="dbba8-117">Constraints</span></span>

<span data-ttu-id="dbba8-118">Si usa el constructor [**RealTimeStylus**](realtimestylus-class.md) predeterminado, se crea un objeto **RealTimeStylus** que solo puede aceptar la entrada de otro objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="dbba8-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="dbba8-119">En la lista siguiente se describen las restricciones asociadas al uso del modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada.</span><span class="sxs-lookup"><span data-stu-id="dbba8-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="dbba8-120">Solo se pueden usar dos objetos [**RealTimeStylus**](realtimestylus-class.md) , un objeto **RealTimeStylus** primario y un objeto **RealTimeStylus** secundario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="dbba8-121">El objeto [**RealTimeStylus**](realtimestylus-class.md) principal se debe crear con un constructor que use el parámetro **attachedControl** o *Handle* .</span><span class="sxs-lookup"><span data-stu-id="dbba8-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="dbba8-122">El objeto **RealTimeStylus** secundario debe crearse con el constructor sin argumentos.</span><span class="sxs-lookup"><span data-stu-id="dbba8-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="dbba8-123">El objeto [**RealTimeStylus**](realtimestylus-class.md) secundario debe ser el único complemento asincrónico de la colección de complementos asincrónica del objeto **RealTimeStylus** principal.</span><span class="sxs-lookup"><span data-stu-id="dbba8-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="dbba8-124">Un objeto [**RealTimeStylus**](realtimestylus-class.md) secundario solo se puede asociar a un objeto **RealTimeStylus** primario a la vez.</span><span class="sxs-lookup"><span data-stu-id="dbba8-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="dbba8-125">Si se agrega a un segundo objeto **RealTimeStylus** primario, el método [Add](/previous-versions/ms824814(v=msdn.10)) produce una excepción y el objeto **RealTimeStylus** secundario no se adjunta al segundo objeto **RealTimeStylus** primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="dbba8-126">Se modifica el comportamiento de algunos de los miembros del objeto [**RealTimeStylus**](realtimestylus-class.md) secundarios.</span><span class="sxs-lookup"><span data-stu-id="dbba8-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="dbba8-127">En la tabla siguiente se describe el comportamiento modificado de estos miembros.</span><span class="sxs-lookup"><span data-stu-id="dbba8-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="dbba8-128">Miembro</span><span class="sxs-lookup"><span data-stu-id="dbba8-128">Member</span></span></th>
    <th><span data-ttu-id="dbba8-129">Comportamiento</span><span class="sxs-lookup"><span data-stu-id="dbba8-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="dbba8-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="dbba8-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="dbba8-131">Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="dbba8-132">Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, este método devuelve el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dbba8-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="dbba8-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="dbba8-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="dbba8-134">Este método genera una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="dbba8-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="dbba8-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="dbba8-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="dbba8-136">Este método devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="dbba8-137">Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, este método devuelve una matriz vacía.</span><span class="sxs-lookup"><span data-stu-id="dbba8-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="dbba8-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="dbba8-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="dbba8-139">Al obtener esta propiedad, se devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="dbba8-140">Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, al obtener esta propiedad se devuelve el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dbba8-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="dbba8-141">Al establecer esta propiedad, se produce una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="dbba8-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="dbba8-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span><span class="sxs-lookup"><span data-stu-id="dbba8-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="dbba8-143">Al obtener esta propiedad, se devuelve la información del objeto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="dbba8-144">Si el <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secundario no está asociado a un objeto <strong>RealTimeStylus</strong> primario, al obtener esta propiedad se devuelve el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dbba8-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="dbba8-145">Al establecer esta propiedad, se produce una excepción <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="dbba8-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="dbba8-146">Se espera que el objeto primario [**RealTimeStylus**](realtimestylus-class.md) deje de funcionar cuando se desecha el **RealTimeStylus** secundario.</span><span class="sxs-lookup"><span data-stu-id="dbba8-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
