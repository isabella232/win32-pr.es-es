---
description: Mergemod.dll proporciona un objeto COM que implementa operaciones de combinación y generación de imágenes de origen para módulos de combinación. El objeto principal implementa interfaces para programas de C/C++ y clientes de automatización, incluidos Visual Basic y VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automatización del módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653060"
---
# <a name="merge-module-automation"></a><span data-ttu-id="29b1f-104">Automatización del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="29b1f-104">Merge Module Automation</span></span>

<span data-ttu-id="29b1f-105">Mergemod.dll proporciona un objeto COM que implementa operaciones de combinación y generación de imágenes de origen para módulos de combinación.</span><span class="sxs-lookup"><span data-stu-id="29b1f-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="29b1f-106">El objeto principal implementa interfaces para programas de C/C++ y clientes de automatización, incluidos Visual Basic y VBScript.</span><span class="sxs-lookup"><span data-stu-id="29b1f-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="29b1f-107">El método preferido para instalar Mergemod.dll es mediante el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="29b1f-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="29b1f-108">El identificador de componente del componente que contiene la interfaz COM Mergemod.dll es {FD153241-37EC-11D2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="29b1f-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="29b1f-109">Se puede usar el mismo binario en todos los sistemas de Windows y el archivo dll se registrará automáticamente a través de regsvr32 en sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="29b1f-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="29b1f-110">Tenga en cuenta que Mergemod.dll requiere que el Msvcrt.dll esté instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="29b1f-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="29b1f-111">Tenga en cuenta que se requiere Mergemod.dll 2,0 para crear [módulos de combinación configurables](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="29b1f-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="29b1f-112">Mergemod.dll versión 2,0 proporciona funcionalidad extendida en tiempo de compilación a través de la interfaz [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .</span><span class="sxs-lookup"><span data-stu-id="29b1f-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="29b1f-113">Este CLSID es compatible con toda la funcionalidad existente de la interfaz [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) proporcionada por Mergemod.dll versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="29b1f-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="29b1f-114">La interfaz predeterminada en el objeto [**Merge**](merge-object.md) de Mergemod.dll 2,0 es la interfaz **IMsmMerge2** en lugar de la interfaz **IMsmMerge** .</span><span class="sxs-lookup"><span data-stu-id="29b1f-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="29b1f-115">Modelo de objetos para Mergemod.dll versión 1,0</span><span class="sxs-lookup"><span data-stu-id="29b1f-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="29b1f-116">Modelo de objetos para Mergemod.dll versión 2,0</span><span class="sxs-lookup"><span data-stu-id="29b1f-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
