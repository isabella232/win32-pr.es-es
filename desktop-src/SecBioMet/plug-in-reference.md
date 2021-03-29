---
title: Referencia del complemento
description: 'Funciones de adaptador, funciones de contenedor y estructuras para crear adaptadores de complementos personalizados de tres tipos: motor, sensor y almacenamiento.'
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API de API Plataforma de biometría de Windows de Plataforma de biometría de Windows, referencia del complemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487014"
---
# <a name="plug-in-reference"></a><span data-ttu-id="afd0c-104">Referencia del complemento</span><span class="sxs-lookup"><span data-stu-id="afd0c-104">Plug-in Reference</span></span>

<span data-ttu-id="afd0c-105">Los dispositivos biométricos se fabrican en una amplia variedad de tipos y configuraciones.</span><span class="sxs-lookup"><span data-stu-id="afd0c-105">Biometric devices are manufactured in a wide variety of types and configurations.</span></span> <span data-ttu-id="afd0c-106">La Plataforma de biometría de Windows incorpora una arquitectura extensible que permite tratar con esta variedad mediante la creación de complementos personalizados. En el centro de esta arquitectura hay un objeto de software denominado unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="afd0c-106">The Windows Biometric Framework incorporates an extensible architecture that enables you to deal with this variety by creating custom plug-ins. At the center of this architecture is a software object called a biometric unit.</span></span> <span data-ttu-id="afd0c-107">Puede pensar en una unidad biométrica como una abstracción que representa un dispositivo biométrico en el marco.</span><span class="sxs-lookup"><span data-stu-id="afd0c-107">You can think of a biometric unit as an abstraction that represents a biometric device to the Framework.</span></span> <span data-ttu-id="afd0c-108">Los componentes de software de complemento denominados adaptadores conectan la unidad biométrica al hardware asociado.</span><span class="sxs-lookup"><span data-stu-id="afd0c-108">Plug-in software components called adapters connect the biometric unit to the associated hardware.</span></span> <span data-ttu-id="afd0c-109">Hay tres tipos de adaptadores que puede crear.</span><span class="sxs-lookup"><span data-stu-id="afd0c-109">There are three types of adapters that you can create.</span></span> <span data-ttu-id="afd0c-110">Un adaptador de motor genera plantillas biométricas a partir de ejemplos capturados, coincide con ejemplos con plantillas existentes e indexa plantillas.</span><span class="sxs-lookup"><span data-stu-id="afd0c-110">An engine adapter generates biometric templates from captured samples, matches samples to existing templates, and indexes templates.</span></span> <span data-ttu-id="afd0c-111">Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar para configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al motor de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="afd0c-111">A sensor adapter wraps a biometric device and provides a standard interface for configuring the sensor, capturing samples, and controlling the flow of biometric data to the processing engine.</span></span> <span data-ttu-id="afd0c-112">Un adaptador de almacenamiento administra las bases de datos de plantilla.</span><span class="sxs-lookup"><span data-stu-id="afd0c-112">A storage adapter manages template databases.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="afd0c-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="afd0c-113">In this section</span></span>



| <span data-ttu-id="afd0c-114">Tema</span><span class="sxs-lookup"><span data-stu-id="afd0c-114">Topic</span></span>                                                                 | <span data-ttu-id="afd0c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="afd0c-115">Description</span></span>                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afd0c-116">Funciones de complemento</span><span class="sxs-lookup"><span data-stu-id="afd0c-116">Plug-in Functions</span></span>](plug-in-functions.md)<br/>                 | <span data-ttu-id="afd0c-117">Funciones que puede usar para crear los complementos de adaptador que componen una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="afd0c-117">Functions you can use to create the adapter plug-ins that make up a biometric unit.</span></span><br/>                                                                     |
| [<span data-ttu-id="afd0c-118">Estructuras de complementos</span><span class="sxs-lookup"><span data-stu-id="afd0c-118">Plug-in Structures</span></span>](plug-in-structures.md)<br/>               | <span data-ttu-id="afd0c-119">Estructuras para el desarrollo de aplicaciones cliente mediante la API de Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="afd0c-119">Structures for client application development by the Windows Biometric Framework API.</span></span><br/>                                                                   |
| [<span data-ttu-id="afd0c-120">Funciones de contenedor de complementos</span><span class="sxs-lookup"><span data-stu-id="afd0c-120">Plug-in Wrapper Functions</span></span>](plug-in-wrapper-functions.md)<br/> | <span data-ttu-id="afd0c-121">Funciones contenedoras que permiten llamar a una función pública en cualquier adaptador conectado a la canalización sin adquirir manualmente un puntero al adaptador.</span><span class="sxs-lookup"><span data-stu-id="afd0c-121">Wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span><br/> |



 

 

 





