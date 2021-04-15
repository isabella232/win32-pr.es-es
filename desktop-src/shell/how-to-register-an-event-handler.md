---
description: Un dispositivo puede generar muchos eventos, y cada evento tiene la opción de ser administrado por uno de varios controladores diferentes.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Cómo registrar un controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985422"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="51e47-103">Cómo registrar un controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="51e47-103">How to Register an Event Handler</span></span>

<span data-ttu-id="51e47-104">Un dispositivo puede generar muchos eventos, y cada evento tiene la opción de ser administrado por uno de varios controladores diferentes.</span><span class="sxs-lookup"><span data-stu-id="51e47-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="51e47-105">En Windows XP, se definen los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="51e47-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="51e47-106">DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-106">DeviceArrival</span></span>
-   <span data-ttu-id="51e47-107">DeviceRemoval</span><span class="sxs-lookup"><span data-stu-id="51e47-107">DeviceRemoval</span></span>
-   <span data-ttu-id="51e47-108">MediaArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-108">MediaArrival</span></span>
-   <span data-ttu-id="51e47-109">MediaRemoval</span><span class="sxs-lookup"><span data-stu-id="51e47-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="51e47-110">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="51e47-110">Instructions</span></span>


<span data-ttu-id="51e47-111">Los controladores de eventos se definen en la clave **EventHandlers** .</span><span class="sxs-lookup"><span data-stu-id="51e47-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="51e47-112">Los valores de una clave del controlador de eventos son los nombres de cada controlador que el usuario debe elegir cuando se detecte el evento.</span><span class="sxs-lookup"><span data-stu-id="51e47-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="51e47-113">No hay ningún valor de datos asociado a estas entradas.</span><span class="sxs-lookup"><span data-stu-id="51e47-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="51e47-114">A continuación se muestra una definición de ejemplo de un controlador de eventos personalizado denominado **MyNewRemovalEventHandler**, que presenta estas posibilidades de controlador al usuario:</span><span class="sxs-lookup"><span data-stu-id="51e47-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="51e47-115">Un controlador que se usará si el evento se detecta en un dispositivo realizado por la empresa llamada Contoso, Inc.</span><span class="sxs-lookup"><span data-stu-id="51e47-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="51e47-116">Un controlador que se usará si el evento se detecta en un dispositivo realizado por la empresa denominada Fabrikam, Inc.</span><span class="sxs-lookup"><span data-stu-id="51e47-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="51e47-117">Controlador que se va a usar en todos los demás casos.</span><span class="sxs-lookup"><span data-stu-id="51e47-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="51e47-118">Una vez definido un controlador de eventos, se debe registrar con un controlador de dispositivo para una de las posibilidades de evento: DeviceArrival, DeviceRemoval, MediaArrival o MediaRemoval.</span><span class="sxs-lookup"><span data-stu-id="51e47-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="51e47-119">MyNewRemovalEventHandler, definido anteriormente, se usa para DeviceRemoval en un controlador de dispositivo personalizado denominado MyDeviceHandler y se define para ese propósito en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="51e47-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="51e47-120">De nuevo, el valor del registro no tiene ningún componente de datos.</span><span class="sxs-lookup"><span data-stu-id="51e47-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="51e47-121">Windows XP predefine el siguiente conjunto de EventHandlers.</span><span class="sxs-lookup"><span data-stu-id="51e47-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="51e47-122">Clave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="51e47-122">EventHandlers key</span></span>        | <span data-ttu-id="51e47-123">Tipo de archivo o medio</span><span class="sxs-lookup"><span data-stu-id="51e47-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="51e47-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="51e47-125">CD-R/CD-RW en blanco</span><span class="sxs-lookup"><span data-stu-id="51e47-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="51e47-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="51e47-127">Archivos de imagen</span><span class="sxs-lookup"><span data-stu-id="51e47-127">Picture files</span></span>                                  |
| <span data-ttu-id="51e47-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="51e47-129">Archivos de música</span><span class="sxs-lookup"><span data-stu-id="51e47-129">Music files</span></span>                                    |
| <span data-ttu-id="51e47-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="51e47-131">Archivos de vídeo</span><span class="sxs-lookup"><span data-stu-id="51e47-131">Video files</span></span>                                    |
| <span data-ttu-id="51e47-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="51e47-133">CD de audio (formato REDBOOK CD con pistas de audio)</span><span class="sxs-lookup"><span data-stu-id="51e47-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="51e47-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="51e47-135">Películas de DVD</span><span class="sxs-lookup"><span data-stu-id="51e47-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="51e47-136">Windows Vista predefine el siguiente conjunto de EventHandlers, además de los anteriores.</span><span class="sxs-lookup"><span data-stu-id="51e47-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="51e47-137">Clave EventHandlers</span><span class="sxs-lookup"><span data-stu-id="51e47-137">EventHandlers key</span></span>              | <span data-ttu-id="51e47-138">Tipo de archivo o medio</span><span class="sxs-lookup"><span data-stu-id="51e47-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="51e47-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="51e47-140">Películas super VideoCD</span><span class="sxs-lookup"><span data-stu-id="51e47-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="51e47-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="51e47-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="51e47-142">Películas VideoCD</span><span class="sxs-lookup"><span data-stu-id="51e47-142">VideoCD movies</span></span>       |



 

 

 



