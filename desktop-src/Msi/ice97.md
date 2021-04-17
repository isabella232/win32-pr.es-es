---
description: ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652791"
---
# <a name="ice97"></a><span data-ttu-id="5f918-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="5f918-103">ICE97</span></span>

<span data-ttu-id="5f918-104">ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="5f918-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="5f918-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="5f918-105">Result</span></span>

<span data-ttu-id="5f918-106">ICE97 expone las siguientes advertencias.</span><span class="sxs-lookup"><span data-stu-id="5f918-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="5f918-107">ADVERTENCIA de ICE97</span><span class="sxs-lookup"><span data-stu-id="5f918-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="5f918-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f918-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="5f918-109">Este componente \[ 1 \] instala el componente compartido en el mismo directorio \[ 2 \] que otro, lo que interrumpe las reglas de componentes si se seleccionan los dos (o más) componentes para la instalación.</span><span class="sxs-lookup"><span data-stu-id="5f918-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="5f918-110">Dos componentes no deben aislar un componente compartido en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="5f918-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="5f918-111">Por ejemplo, Component1 y Component2, que comparten ComponentShared, se instalan en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="5f918-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="5f918-112">Ambos especifican ComponentShared como un componente aislado.</span><span class="sxs-lookup"><span data-stu-id="5f918-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="5f918-113">Debido al aislamiento, los archivos de ComponentShared se copian dos veces en la \_ referencia de directorio para Component1 y Component2.</span><span class="sxs-lookup"><span data-stu-id="5f918-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="5f918-114">Los componentes ahora tienen un recuento de referencias en la copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="5f918-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="5f918-115">Esto infringe las reglas del componente instalador.</span><span class="sxs-lookup"><span data-stu-id="5f918-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="5f918-116">Si se desinstala Component1, se quitan los archivos de componentes aislados y Component2 se rompe.</span><span class="sxs-lookup"><span data-stu-id="5f918-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f918-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f918-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f918-118">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="5f918-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



