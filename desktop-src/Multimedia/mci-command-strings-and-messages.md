---
title: Mensajes y cadenas de comandos MCI
description: Mensajes y cadenas de comandos MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Cadenas de comandos MCI, acerca de
- Mensajes de comandos de MCI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904608"
---
# <a name="mci-command-strings-and-messages"></a><span data-ttu-id="d75db-105">Mensajes y cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="d75db-105">MCI Command Strings and Messages</span></span>

<span data-ttu-id="d75db-106">MCI admite [cadenas de comandos](command-strings.md) y [mensajes de comandos](command-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d75db-106">MCI supports [Command Strings](command-strings.md) and [Command Messages](command-messages.md).</span></span> <span data-ttu-id="d75db-107">Puede usar cadenas o mensajes, o ambos, en la aplicación MCI.</span><span class="sxs-lookup"><span data-stu-id="d75db-107">You can use either strings or messages, or both, in your MCI application.</span></span>

-   <span data-ttu-id="d75db-108">La *interfaz de mensajes de comandos* consta de constantes y estructuras.</span><span class="sxs-lookup"><span data-stu-id="d75db-108">The *command-message interface* consists of constants and structures.</span></span> <span data-ttu-id="d75db-109">Use la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar mensajes a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d75db-109">Use the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send messages to an MCI device.</span></span>
-   <span data-ttu-id="d75db-110">La *interfaz de cadena de comandos* proporciona una versión textual de los mensajes de comandos.</span><span class="sxs-lookup"><span data-stu-id="d75db-110">The *command-string interface* provides a textual version of the command messages.</span></span> <span data-ttu-id="d75db-111">Use la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) para enviar cadenas a un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d75db-111">Use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function to send strings to an MCI device.</span></span> <span data-ttu-id="d75db-112">Las cadenas de comandos duplican la funcionalidad de los mensajes de comandos.</span><span class="sxs-lookup"><span data-stu-id="d75db-112">Command strings duplicate the functionality of the command messages.</span></span> <span data-ttu-id="d75db-113">El sistema operativo convierte las cadenas de comandos en mensajes de comandos antes de enviarlos al controlador MCI para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="d75db-113">The operating system converts the command strings to command messages before sending them to the MCI driver for processing.</span></span>

<span data-ttu-id="d75db-114">Los mensajes de comandos que recuperan información lo hacen en forma de estructuras, que son fáciles de interpretar en una aplicación de C.</span><span class="sxs-lookup"><span data-stu-id="d75db-114">The command messages that retrieve information do so in the form of structures, which are easy to interpret in a C application.</span></span> <span data-ttu-id="d75db-115">Estas estructuras pueden contener información sobre muchos aspectos diferentes de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d75db-115">These structures can contain information on many different aspects of a device.</span></span> <span data-ttu-id="d75db-116">Las cadenas de comandos que recuperan información lo hacen en forma de cadenas y solo pueden recuperar una cadena cada vez.</span><span class="sxs-lookup"><span data-stu-id="d75db-116">The command strings that retrieve information do so in the form of strings, and can only retrieve one string at a time.</span></span> <span data-ttu-id="d75db-117">La aplicación debe analizar o probar cada cadena para interpretarla.</span><span class="sxs-lookup"><span data-stu-id="d75db-117">Your application must parse or test each string to interpret it.</span></span> <span data-ttu-id="d75db-118">Es posible que los mensajes de comando sean más fáciles de usar que las cadenas de comandos en algunos casos, pero las cadenas de comandos son fáciles de recordar e implementar.</span><span class="sxs-lookup"><span data-stu-id="d75db-118">You might find that the command messages are easier to use than the command strings in some cases, but the command strings are easy to remember and implement.</span></span> <span data-ttu-id="d75db-119">Algunas aplicaciones MCI usan cadenas de comandos cuando el valor devuelto no se usará (excepto para comprobar que se ha realizado correctamente) y mensajes de comando al recuperar información del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d75db-119">Some MCI applications use command strings when the return value will not be used (other than to verify success) and command messages when retrieving information from the device.</span></span>

<span data-ttu-id="d75db-120">Cuando se analizan los comandos, en esta información general se usa el formato de cadena del comando seguido del formulario de mensaje entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="d75db-120">When commands are discussed, this overview uses the string form of the command followed by the message form in parentheses.</span></span>

 

 