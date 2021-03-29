---
description: Evalcom2.dll puede usarse para implementar operaciones de validación de paquetes de instalación y módulos de combinación mediante evaluadores de coherencia internos (CIEM).
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Usar Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809920"
---
# <a name="using-evalcom2"></a><span data-ttu-id="23a84-103">Usar Evalcom2</span><span class="sxs-lookup"><span data-stu-id="23a84-103">Using Evalcom2</span></span>

<span data-ttu-id="23a84-104">Evalcom2.dll puede usarse para implementar operaciones de validación de paquetes de instalación y módulos de combinación mediante [evaluadores de coherencia internos (CIEM)](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="23a84-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="23a84-105">El objeto principal implementa interfaces para programas de C/C++.</span><span class="sxs-lookup"><span data-stu-id="23a84-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="23a84-106">El objeto principal también implementa [interfaces Evalcom2](evalcom2-interfaces.md) para programas de C/C++.</span><span class="sxs-lookup"><span data-stu-id="23a84-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="23a84-107">El CLSID necesario para obtener la interfaz de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) es {6E5E1910-8053-4660-B795-6B612E29BC58}.</span><span class="sxs-lookup"><span data-stu-id="23a84-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="23a84-108">REFIID es {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span><span class="sxs-lookup"><span data-stu-id="23a84-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="23a84-109">Puede usar el siguiente procedimiento para implementar las operaciones de validación.</span><span class="sxs-lookup"><span data-stu-id="23a84-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="23a84-110">**Para implementar operaciones de validación**</span><span class="sxs-lookup"><span data-stu-id="23a84-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="23a84-111">Inicialice COM en el subproceso que realiza la llamada con [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="23a84-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="23a84-112">Obtenga el puntero a la interfaz [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="23a84-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="23a84-113">Abra el paquete de instalación o el módulo de combinación mediante el método [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .</span><span class="sxs-lookup"><span data-stu-id="23a84-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="23a84-114">Abra el archivo de evaluación mediante el método [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .</span><span class="sxs-lookup"><span data-stu-id="23a84-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="23a84-115">Establezca la función de devolución de llamada de presentación mediante el método [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .</span><span class="sxs-lookup"><span data-stu-id="23a84-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="23a84-116">Establezca la función de devolución de llamada de estado mediante el método [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="23a84-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="23a84-117">Realice la validación mediante el método [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .</span><span class="sxs-lookup"><span data-stu-id="23a84-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="23a84-118">Cierre el archivo. Cub con el método [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .</span><span class="sxs-lookup"><span data-stu-id="23a84-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="23a84-119">Cierre la base de datos mediante el método [**CerrarBaseDeDatos**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="23a84-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="23a84-120">Libere la interfaz [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .</span><span class="sxs-lookup"><span data-stu-id="23a84-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="23a84-121">Anular la inicialización de COM mediante [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="23a84-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23a84-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23a84-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23a84-123">Interfaces Evalcom2</span><span class="sxs-lookup"><span data-stu-id="23a84-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="23a84-124">Automatización de la validación</span><span class="sxs-lookup"><span data-stu-id="23a84-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="23a84-125">Funciones de devolución de llamada de validación</span><span class="sxs-lookup"><span data-stu-id="23a84-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
