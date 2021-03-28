---
title: Interfaces de versión comunes
description: Esta sección contiene información sobre las interfaces de versión comunes.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2020
ms.locfileid: "103797163"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="20a1d-103">Interfaces de versión comunes</span><span class="sxs-lookup"><span data-stu-id="20a1d-103">Common version interfaces</span></span>

<span data-ttu-id="20a1d-104">Esta sección contiene información sobre las interfaces de versión comunes.</span><span class="sxs-lookup"><span data-stu-id="20a1d-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="20a1d-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="20a1d-105">In this section</span></span>

| <span data-ttu-id="20a1d-106">Tema</span><span class="sxs-lookup"><span data-stu-id="20a1d-106">Topic</span></span> | <span data-ttu-id="20a1d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="20a1d-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="20a1d-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="20a1d-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="20a1d-109">Esta interfaz se usa para devolver datos de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="20a1d-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="20a1d-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20a1d-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="20a1d-111">Esta interfaz se usa para devolver datos de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="20a1d-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="20a1d-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="20a1d-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="20a1d-113">Se usa para registrarse en las devoluciones de llamada cuando se destruye un objeto nano-COM de 3D directo.</span><span class="sxs-lookup"><span data-stu-id="20a1d-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="20a1d-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="20a1d-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="20a1d-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) es una interfaz de inclusión que el usuario implementa para permitir que una aplicación llame a métodos reemplazables por el usuario para abrir y cerrar archivos de inclusión de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="20a1d-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="20a1d-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="20a1d-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="20a1d-117">La interfaz [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) permite a una aplicación describir secciones conceptuales y marcadores en el flujo de código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20a1d-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="20a1d-118">Una herramienta habilitada correctamente, como Microsoft Visual Studio Ultimate 2012, puede mostrar estas secciones y marcadores visualmente a lo largo de la línea de tiempo de Microsoft Direct3D de la herramienta, mientras que la herramienta depura la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20a1d-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="20a1d-119">Estas notas visuales permiten a los usuarios de una herramienta de este tipo navegar a partes de la línea de tiempo que son de interés, o a entender qué conjunto de llamadas de Direct3D se producen en determinadas secciones del código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20a1d-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="20a1d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20a1d-120">Related topics</span></span>

[<span data-ttu-id="20a1d-121">Referencia de la versión común</span><span class="sxs-lookup"><span data-stu-id="20a1d-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
