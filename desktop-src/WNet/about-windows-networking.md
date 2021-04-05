---
title: Acerca de las redes de Windows
description: Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información acerca de la configuración actual de la red.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows Networking WNet, descrito
- WNet WNet, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076328"
---
# <a name="about-windows-networking"></a><span data-ttu-id="6ab2a-105">Acerca de las redes de Windows</span><span class="sxs-lookup"><span data-stu-id="6ab2a-105">About Windows Networking</span></span>

<span data-ttu-id="6ab2a-106">Las aplicaciones pueden usar las funciones de WNet para agregar y cancelar conexiones de red y para recuperar información acerca de la configuración actual de la red.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="6ab2a-107">En la ilustración siguiente se muestra la estructura de una red típica.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-107">The following figure shows the structure of a typical network.</span></span>

![estructura de red típica](images/csnet-01.png)

<span data-ttu-id="6ab2a-109">En la ilustración anterior, la jerarquía de los recursos de Windows NT Server/Windows 2000 Server se proporciona en detalle como proveedor de red \# 1.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="6ab2a-110">Los recursos de red de otros proveedores tienen diferentes sistemas jerárquicos.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="6ab2a-111">Una aplicación no necesita información sobre la jerarquía antes de empezar a trabajar con una red.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="6ab2a-112">Puede continuar desde la raíz de red (es decir, el recurso de contenedor de nivel superior) y recuperar información acerca de los recursos de la red a medida que se requiere la información.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="6ab2a-113">Los recursos de red que contienen otros recursos se denominan *contenedores*.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="6ab2a-114">Los recursos de contenedor se encuentran en los cuadros de la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="6ab2a-115">Los recursos que no contienen otros recursos se denominan *objetos*.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="6ab2a-116">En la ilustración anterior, SharePoint \# 1 y SharePoint \# 2 son objetos.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="6ab2a-117">Un *SharePoint* es un objeto al que se puede tener acceso a través de la red.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="6ab2a-118">Entre los ejemplos de SharePoint se incluyen impresoras y directorios compartidos.</span><span class="sxs-lookup"><span data-stu-id="6ab2a-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




