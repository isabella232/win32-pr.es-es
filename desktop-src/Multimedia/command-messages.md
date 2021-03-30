---
title: Mensajes de comando
description: Mensajes de comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Mensajes de comandos de MCI, acerca de
- Mensajes de comandos MCI, sintaxis
- mciSendCommand función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533100"
---
# <a name="command-messages"></a><span data-ttu-id="ad96a-106">Mensajes de comando</span><span class="sxs-lookup"><span data-stu-id="ad96a-106">Command Messages</span></span>

<span data-ttu-id="ad96a-107">La interfaz de mensajes de comandos está diseñada para que la utilicen las aplicaciones que requieren una interfaz de lenguaje C para controlar los dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="ad96a-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="ad96a-108">Utiliza un paradigma de paso de mensajes para comunicarse con dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="ad96a-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="ad96a-109">Puede enviar un comando mediante la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad96a-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="ad96a-110">La función **mciSendCommand** devuelve cero si es correcto.</span><span class="sxs-lookup"><span data-stu-id="ad96a-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="ad96a-111">Si se produce un error en la función, la palabra de orden inferior del valor devuelto contiene un código de error.</span><span class="sxs-lookup"><span data-stu-id="ad96a-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="ad96a-112">Este código de error se puede pasar a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.</span><span class="sxs-lookup"><span data-stu-id="ad96a-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="ad96a-113">Sintaxis de los mensajes de comandos</span><span class="sxs-lookup"><span data-stu-id="ad96a-113">Syntax of Command Messages</span></span>

<span data-ttu-id="ad96a-114">Los mensajes de comandos MCI constan de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ad96a-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="ad96a-115">Un valor de mensaje constante</span><span class="sxs-lookup"><span data-stu-id="ad96a-115">A constant message value</span></span>
-   <span data-ttu-id="ad96a-116">Estructura que contiene los parámetros del comando.</span><span class="sxs-lookup"><span data-stu-id="ad96a-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="ad96a-117">Un conjunto de marcadores que especifican las opciones del comando y validan los campos en el bloque de parámetros.</span><span class="sxs-lookup"><span data-stu-id="ad96a-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="ad96a-118">En el ejemplo siguiente se usa la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar el comando [**MCI \_ Play**](mci-play.md) al dispositivo identificado mediante un identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad96a-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="ad96a-119">El identificador de dispositivo proporcionado en el primer parámetro se recupera cuando el dispositivo se abre con el comando [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="ad96a-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="ad96a-120">El último parámetro es la dirección de una estructura de [**\_ \_ parms de reproducción de MCI**](mci-play-parms.md) , que podría contener información sobre dónde empezar y finalizar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ad96a-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="ad96a-121">Muchos mensajes de comando de MCI usan una estructura para contener parámetros de este tipo.</span><span class="sxs-lookup"><span data-stu-id="ad96a-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="ad96a-122">El primer miembro de cada una de estas estructuras identifica la ventana que recibe un mensaje [**mm \_ MCINOTIFY**](mm-mcinotify.md) cuando finaliza la operación.</span><span class="sxs-lookup"><span data-stu-id="ad96a-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 