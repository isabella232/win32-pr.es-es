---
title: Arranque medido
description: Arranque medido
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314346"
---
# <a name="measured-boot"></a><span data-ttu-id="e6c1d-103">Arranque medido</span><span class="sxs-lookup"><span data-stu-id="e6c1d-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="e6c1d-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="e6c1d-104">Platforms</span></span>

 <span data-ttu-id="e6c1d-105">**Clientes:** Windows 8</span><span class="sxs-lookup"><span data-stu-id="e6c1d-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="e6c1d-106">**Servidores:** Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6c1d-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="e6c1d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6c1d-107">Description</span></span>

<span data-ttu-id="e6c1d-108">A medida que el software antimalware (AM) se ha vuelto mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también están mejorando en la creación de rootkits que pueden ocultarse de la detección.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="e6c1d-109">Detectar malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM abordan diligentemente.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="e6c1d-110">Normalmente, crean hacks del sistema que no son compatibles con el sistema operativo host y pueden dar lugar realmente a la colocación del equipo en un estado inestable.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="e6c1d-111">Hasta este momento, Windows no ha proporcionado una buena manera de que AM detecte y resuelva estas amenazas de arranque temprano.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="e6c1d-112">Windows 8 presenta una nueva característica denominada Arranque medido, que mide cada componente, desde el firmware hasta los controladores de inicio de arranque, almacena esas medidas en el Módulo de plataforma segura (TPM) en la máquina y, a continuación, pone a disposición un registro que se puede probar de forma remota para comprobar el estado de arranque del cliente.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="e6c1d-113">Manifestación</span><span class="sxs-lookup"><span data-stu-id="e6c1d-113">Manifestation</span></span>

<span data-ttu-id="e6c1d-114">La Arranque medido proporciona software de AM con un registro de confianza (resistente a la suplantación y manipulación) de todos los componentes de arranque que se iniciaron antes del software de AM.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="e6c1d-115">El software de AM puede usar el registro para determinar si los componentes que se han ejecutado antes son de confianza o si están infectados con malware.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="e6c1d-116">El software am del equipo local puede enviar el registro a un servidor remoto para su evaluación.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-116">The AM software on the local machine can send the log to a remote server for evaluation.</span></span> <span data-ttu-id="e6c1d-117">El servidor remoto puede iniciar acciones de corrección mediante la interacción con el software en el cliente o a través de mecanismos fuera de banda, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="e6c1d-118">Mitigación</span><span class="sxs-lookup"><span data-stu-id="e6c1d-118">Mitigation</span></span>

<span data-ttu-id="e6c1d-119">En escenarios empresariales, el administrador del sistema tiene el control de Arranque medido se usa la información.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="e6c1d-120">En escenarios de usuario final, por ejemplo, la banca en línea), el consumidor debe optar por usar Arranque medido para el servicio específico.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="e6c1d-121">Solución</span><span class="sxs-lookup"><span data-stu-id="e6c1d-121">Solution</span></span>

<span data-ttu-id="e6c1d-122">Se está preparando una documentación que detalla las API y las llamadas de función que se deben realizar para varios Arranque medido escenarios.</span><span class="sxs-lookup"><span data-stu-id="e6c1d-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




