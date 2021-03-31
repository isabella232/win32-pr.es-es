---
description: El propósito de un archivo DLL de GINA es proporcionar procedimientos de autenticación e identificación de usuario personalizables. El GINA predeterminado lo hace mediante la delegación de la supervisión de eventos SAS en Winlogon, que recibe y procesa las secuencias de atención segura de CTL + ALT + Supr (SASs).
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816046"
---
# <a name="gina"></a><span data-ttu-id="f45d1-104">GINA</span><span class="sxs-lookup"><span data-stu-id="f45d1-104">GINA</span></span>

<span data-ttu-id="f45d1-105">[*Gina*](/windows/desktop/SecGloss/g-gly) funciona en el [*contexto*](/windows/desktop/SecGloss/c-gly) del proceso [*Winlogon*](/windows/desktop/SecGloss/w-gly) y, como tal, el archivo dll de Gina se carga muy pronto en el proceso de arranque.</span><span class="sxs-lookup"><span data-stu-id="f45d1-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="f45d1-106">El archivo DLL de GINA debe cumplir las reglas para que se mantenga la integridad del sistema, especialmente con respecto a la interacción con el usuario.</span><span class="sxs-lookup"><span data-stu-id="f45d1-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="f45d1-107">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f45d1-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="f45d1-108">El uso más común de GINA es comunicarse con un dispositivo externo como un [*lector*](/windows/desktop/SecGloss/r-gly)de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="f45d1-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="f45d1-109">Es esencial establecer el parámetro Start del controlador de dispositivo en System (Winnt. h: SERVICE \_ System \_ Start) para asegurarse de que el controlador se carga en el momento en que se invoca gina.</span><span class="sxs-lookup"><span data-stu-id="f45d1-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="f45d1-110">El propósito de un archivo DLL de GINA es proporcionar procedimientos de autenticación e identificación de usuario personalizables.</span><span class="sxs-lookup"><span data-stu-id="f45d1-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="f45d1-111">El GINA predeterminado lo hace mediante la delegación de la supervisión de eventos SAS en Winlogon, que recibe y procesa las [*secuencias de atención segura*](/windows/desktop/SecGloss/s-gly) de CTL + Alt + Supr (Sass).</span><span class="sxs-lookup"><span data-stu-id="f45d1-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="f45d1-112">Una GINA personalizada es responsable de configurarse para recibir eventos SAS (distintos del evento predeterminado CTRL + ALT + Supr) y notificar a Winlogon cuando se producen eventos SAS.</span><span class="sxs-lookup"><span data-stu-id="f45d1-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="f45d1-113">Winlogon evaluará su estado para determinar lo que se necesita para procesar la SAS de GINA personalizada.</span><span class="sxs-lookup"><span data-stu-id="f45d1-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="f45d1-114">Normalmente, este procesamiento incluye llamadas a las funciones de procesamiento de SAS de GINA.</span><span class="sxs-lookup"><span data-stu-id="f45d1-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="f45d1-115">Para obtener información sobre las funciones de exportación de GINA específicas, consulte [funciones de exportación de Gina](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f45d1-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="f45d1-116">Para obtener información sobre el uso de estructuras GINA para pasar información, consulte [estructuras Gina](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="f45d1-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="f45d1-117">Tema</span><span class="sxs-lookup"><span data-stu-id="f45d1-117">Topic</span></span>                                                                             | <span data-ttu-id="f45d1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f45d1-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f45d1-119">Cargar y ejecutar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="f45d1-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="f45d1-120">El valor de clave del registro que se va a modificar para cargar y ejecutar un archivo DLL de GINA personalizado.</span><span class="sxs-lookup"><span data-stu-id="f45d1-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="f45d1-121">Compilar y probar un archivo DLL de GINA</span><span class="sxs-lookup"><span data-stu-id="f45d1-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="f45d1-122">Cómo probar un archivo DLL de GINA.</span><span class="sxs-lookup"><span data-stu-id="f45d1-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

