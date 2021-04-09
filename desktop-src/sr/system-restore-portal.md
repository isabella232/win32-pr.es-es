---
title: Restaurar sistema
description: Establece los puntos de restauración del sistema y supervisa los cambios del sistema de claves de un programa para permitir la reversión del sistema a un estado anterior. Escriba el código de recuperación automática o el script de WMI para restaurar el estado del sistema en un punto de restauración registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restaurar sistema
- Restaurar sistema, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149420"
---
# <a name="system-restore"></a><span data-ttu-id="176ba-106">Restaurar sistema</span><span class="sxs-lookup"><span data-stu-id="176ba-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="176ba-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="176ba-107">Purpose</span></span>

<span data-ttu-id="176ba-108">Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="176ba-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="176ba-109">Está diseñado para reducir los costos de soporte técnico y aumentar la satisfacción del cliente al permitir que un usuario deshaga un cambio que puede haber causado un problema en el sistema o revertir a un día en el que el sistema funcionaba de forma óptima.</span><span class="sxs-lookup"><span data-stu-id="176ba-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="176ba-110">La siguiente documentación está dirigida a los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="176ba-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="176ba-111">Si es un usuario final que busca información sobre cómo usar Restaurar sistema, consulte [¿Qué es restaurar sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="176ba-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="176ba-112">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="176ba-112">Developer audience</span></span>

<span data-ttu-id="176ba-113">La API de restauración del sistema está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="176ba-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="176ba-114">Es necesario estar familiarizado con Instrumental de administración de Windows (WMI) para usar la interfaz de scripting.</span><span class="sxs-lookup"><span data-stu-id="176ba-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="176ba-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="176ba-115">Run-time requirements</span></span>

<span data-ttu-id="176ba-116">La API de restauración del sistema se admite en sistemas operativos de cliente a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="176ba-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="176ba-117">Para obtener información sobre los sistemas operativos necesarios para usar un elemento de API determinado, consulte la sección de requisitos de la documentación.</span><span class="sxs-lookup"><span data-stu-id="176ba-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="176ba-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="176ba-118">In this section</span></span>



| <span data-ttu-id="176ba-119">Tema</span><span class="sxs-lookup"><span data-stu-id="176ba-119">Topic</span></span>                                                | <span data-ttu-id="176ba-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="176ba-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="176ba-121">Información general</span><span class="sxs-lookup"><span data-stu-id="176ba-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="176ba-122">Información general sobre cómo funciona la restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="176ba-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="176ba-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="176ba-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="176ba-124">Documentación de las funciones, estructuras y clases de restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="176ba-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="176ba-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="176ba-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="176ba-126">Programa de ejemplo escrito en C.</span><span class="sxs-lookup"><span data-stu-id="176ba-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="176ba-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="176ba-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="176ba-128">WMI</span><span class="sxs-lookup"><span data-stu-id="176ba-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

