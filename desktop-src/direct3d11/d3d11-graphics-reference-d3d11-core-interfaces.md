---
title: Interfaces principales de Direct3D 11
description: Esta sección contiene información sobre las interfaces principales.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488426"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="ce209-104">Interfaces principales de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ce209-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="ce209-105">Esta sección contiene información sobre las interfaces principales.</span><span class="sxs-lookup"><span data-stu-id="ce209-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce209-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ce209-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce209-107">Tema</span><span class="sxs-lookup"><span data-stu-id="ce209-107">Topic</span></span></th>
<th><span data-ttu-id="ce209-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce209-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce209-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-110">Esta interfaz encapsula los métodos para recuperar datos de la GPU de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ce209-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-112">La interfaz de estado de Blend contiene una descripción del estado de mezcla que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-114">La interfaz de estado de Blend contiene una descripción del estado de mezcla que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="ce209-115">Esta interfaz de estado de Blend admite operaciones lógicas, así como operaciones de fusión.</span><span class="sxs-lookup"><span data-stu-id="ce209-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-117">La interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsula una lista de comandos de gráficos para reproducir.</span><span class="sxs-lookup"><span data-stu-id="ce209-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-119">Esta interfaz encapsula métodos para medir el rendimiento de la GPU.</span><span class="sxs-lookup"><span data-stu-id="ce209-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-121">La interfaz Depth-cliché-State contiene una descripción del estado de la galería de símbolos de profundidad que se puede enlazar a la <a href="d3d10-graphics-programming-guide-output-merger-stage.md">fase de combinación de salida</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-123">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-125">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="ce209-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-128">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="ce209-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-131">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="ce209-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-134">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="ce209-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, como <strong>RegisterDeviceRemovedEvent</strong> y <strong>UnregisterDeviceRemoved</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce209-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-137">La interfaz de dispositivo representa un adaptador virtual; se usa para crear recursos.</span><span class="sxs-lookup"><span data-stu-id="ce209-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="ce209-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-140">Una interfaz de dispositivo-secundario obtiene acceso a los datos que usa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce209-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-142">La interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> representa un contexto de dispositivo que genera comandos de representación.</span><span class="sxs-lookup"><span data-stu-id="ce209-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ce209-143">La versión más reciente de esta interfaz es <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introducida en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="ce209-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="ce209-144">Las aplicaciones destino Windows 10 Creators Update deben usar la interfaz <strong>ID3D11DeviceContext4</strong> en lugar de <strong>ID3D11Device</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce209-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-146">La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos.</span><span class="sxs-lookup"><span data-stu-id="ce209-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="ce209-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-149">La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos.</span><span class="sxs-lookup"><span data-stu-id="ce209-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="ce209-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-152">La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos.</span><span class="sxs-lookup"><span data-stu-id="ce209-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="ce209-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-155">La interfaz de contexto de dispositivo representa un contexto de dispositivo. se utiliza para representar comandos.</span><span class="sxs-lookup"><span data-stu-id="ce209-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="ce209-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> agrega nuevos métodos a los de <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-158">La interfaz <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> representa un objeto de estado de contexto, que contiene información sobre el estado y el comportamiento de un dispositivo de Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ce209-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-160">Representa una barrera, un objeto que se usa para la sincronización de la CPU y una o varias GPU.</span><span class="sxs-lookup"><span data-stu-id="ce209-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-162">Una interfaz de diseño de entrada contiene una definición de cómo alimentar los datos de vértices que se colocan en la memoria en la <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">fase de ensamblador de entrada</a> de la <a href="overviews-direct3d-11-graphics-pipeline.md">canalización de gráficos</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-164">Proporciona protección de subprocesos para las secciones críticas de una aplicación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="ce209-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-166">Una interfaz de predicado determina si la geometría se debe procesar en función de los resultados de una llamada a Draw anterior.</span><span class="sxs-lookup"><span data-stu-id="ce209-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-168">Una interfaz de consulta consulta información de la GPU.</span><span class="sxs-lookup"><span data-stu-id="ce209-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-170">Representa un objeto de consulta para consultar información de la unidad de procesamiento de gráficos (GPU).</span><span class="sxs-lookup"><span data-stu-id="ce209-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-172">La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-174">La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="ce209-175">Esta interfaz de estado de rasterizador admite el recuento de muestras forzada.</span><span class="sxs-lookup"><span data-stu-id="ce209-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce209-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-177">La interfaz de estado de rasterizador contiene una descripción del estado de rasterizador que puede enlazar a la <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">fase de rasterizador</a>.</span><span class="sxs-lookup"><span data-stu-id="ce209-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="ce209-178">Esta interfaz de estado de rasterizador admite el recuento de muestras forzada y el modo de rasterización conservador.</span><span class="sxs-lookup"><span data-stu-id="ce209-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce209-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="ce209-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="ce209-180">La interfaz de estado de muestra contiene una descripción de estado de muestra que se puede enlazar a cualquier fase del sombreador de la <a href="overviews-direct3d-11-graphics-pipeline.md">canalización</a> como referencia a las operaciones de ejemplo de textura.</span><span class="sxs-lookup"><span data-stu-id="ce209-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce209-181">Direct3D 11 implementa interfaces para:</span><span class="sxs-lookup"><span data-stu-id="ce209-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="ce209-182">Recursos</span><span class="sxs-lookup"><span data-stu-id="ce209-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="ce209-183">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="ce209-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="ce209-184">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce209-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce209-185">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="ce209-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

