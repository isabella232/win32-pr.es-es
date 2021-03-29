---
title: Métodos abreviados de comandos y variaciones
description: Métodos abreviados de comandos y variaciones
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778066"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="5bfbf-103">Métodos abreviados de comandos y variaciones</span><span class="sxs-lookup"><span data-stu-id="5bfbf-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="5bfbf-104">Puede usar varios métodos abreviados al trabajar con comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="5bfbf-105">Estos métodos abreviados le permiten usar un único identificador para hacer referencia a todos los dispositivos que ha abierto la aplicación, o para abrir un dispositivo sin emitir explícitamente un comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="5bfbf-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="5bfbf-106">Puede especificar "All" (MCI \_ All \_ Device \_ ID) como un identificador de dispositivo para cualquier comando que no devuelva información.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="5bfbf-107">Cuando se especifica "All", MCI envía el comando secuencialmente a todos los dispositivos abiertos por la aplicación actual.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="5bfbf-108">Por ejemplo, el comando [**cerrar**](close.md) "todo" cierra todos los dispositivos abiertos y el comando [**reproducir**](play.md) "todo" comienza a reproducir todos los dispositivos abiertos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="5bfbf-109">Dado que MCI envía secuencialmente los comandos a los dispositivos MCI, hay un intervalo entre el momento en que el primer y el último dispositivo reciben el comando.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="5bfbf-110">El uso de "todo" es una manera cómoda de difundir un comando a todos los dispositivos, pero no debe confiar en él para sincronizar los dispositivos. el tiempo entre los mensajes puede variar.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="5bfbf-111">Cuando se emite un comando y se especifica un dispositivo que no está abierto, MCI intenta abrir el dispositivo antes de implementar el comando.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="5bfbf-112">Las siguientes reglas se aplican a la apertura automática de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="5bfbf-113">La característica de apertura automática solo funciona con la interfaz de la cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="5bfbf-114">Se produce un error en la característica de apertura automática para los comandos que son específicos de los controladores de dispositivos personalizados.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="5bfbf-115">Los dispositivos abiertos automáticamente no responden a los comandos que usan "All" como nombre de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="5bfbf-116">La característica de apertura automática no permite que la aplicación especifique la marca "tipo".</span><span class="sxs-lookup"><span data-stu-id="5bfbf-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="5bfbf-117">Sin el nombre del dispositivo, MCI determina el nombre del dispositivo a partir de las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="5bfbf-118">Para usar un dispositivo específico, puede combinar el nombre del dispositivo con el nombre de archivo mediante el signo de exclamación, como se describe en el material de referencia del comando [**Open**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="5bfbf-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="5bfbf-119">Si una aplicación usa la característica de apertura automática para abrir un dispositivo, la aplicación debe comprobar el valor devuelto de cada comando abierto subsiguiente para comprobar que el dispositivo sigue abierto.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="5bfbf-120">MCI también cierra automáticamente cualquier dispositivo que se abre automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="5bfbf-121">MCI normalmente cierra un dispositivo en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="5bfbf-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="5bfbf-122">El comando se ha completado.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-122">The command is completed.</span></span>
-   <span data-ttu-id="5bfbf-123">Anula el comando.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-123">You abort the command.</span></span>
-   <span data-ttu-id="5bfbf-124">La notificación se solicita en un comando posterior.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="5bfbf-125">MCI detecta un error.</span><span class="sxs-lookup"><span data-stu-id="5bfbf-125">MCI detects a failure.</span></span>

 

 




