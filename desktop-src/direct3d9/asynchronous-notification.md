---
description: Hay un número de consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notificación asincrónica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705313"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="c0e32-103">Notificación asincrónica (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0e32-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="c0e32-104">Hay un número de consultas interesantes en un controlador que una aplicación puede realizar si no hay ningún costo de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c0e32-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="c0e32-105">En Direct3D 7 y Direct3D 8, un mecanismo de consulta sincrónico, GetInfo, funcionó bien para cosas como las estadísticas, pero no se agregaron consultas críticas para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c0e32-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="c0e32-106">Hay otras cosas (como barreras) que son intrínsecamente asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="c0e32-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="c0e32-107">Se trata de una API sencilla para realizar consultas sincrónicas y asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="c0e32-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="c0e32-108">Las GetInfo se retirarán en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c0e32-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="c0e32-109">Cree una consulta mediante [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="c0e32-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="c0e32-110">Este método toma un D3DQUERYTYPE, que define el tipo de consulta que se va a realizar y devuelve un puntero a un objeto [**IDirect3DQuery9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="c0e32-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="c0e32-111">Si no se admite el tipo de consulta, la llamada devuelve un error D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c0e32-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="c0e32-112">Mediante el objeto de consulta, la aplicación envía la consulta al tiempo de ejecución mediante [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)y sondea el estado de la consulta mediante [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="c0e32-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="c0e32-113">Si el resultado de la consulta está disponible, \_ se devuelve un valor correcto; de lo contrario, \_ se devuelve s.</span><span class="sxs-lookup"><span data-stu-id="c0e32-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="c0e32-114">Se espera que la aplicación pase un búfer de tamaño adecuado para los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="c0e32-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="c0e32-115">La aplicación tiene una opción para obligar al tiempo de ejecución a vaciar la consulta hasta el controlador mediante el \_ vaciado de D3DGETDATA con [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="c0e32-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="c0e32-116">Provoca un vaciado, forzando al controlador a ver la consulta.</span><span class="sxs-lookup"><span data-stu-id="c0e32-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="c0e32-117">En este caso, \_ se devuelve D3DERR DEVICELOST si se pierde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0e32-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="c0e32-118">Todas las consultas se pierden cuando se pierde el dispositivo, la aplicación tiene que volver a crearlas.</span><span class="sxs-lookup"><span data-stu-id="c0e32-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="c0e32-119">Si el dispositivo no admite la consulta y el valor de pQueryID es **null**, se producirá un error en la creación de la consulta con D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c0e32-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c0e32-120">En la tabla siguiente se resume información importante acerca de cada tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="c0e32-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="c0e32-121">QuertyType</span><span class="sxs-lookup"><span data-stu-id="c0e32-121">QuertyType</span></span>                    | <span data-ttu-id="c0e32-122">Marca de problema válida</span><span class="sxs-lookup"><span data-stu-id="c0e32-122">Valid issue flag</span></span>              | <span data-ttu-id="c0e32-123">Búfer GetData</span><span class="sxs-lookup"><span data-stu-id="c0e32-123">GetData buffer</span></span>              | <span data-ttu-id="c0e32-124">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="c0e32-124">Runtime</span></span>      | <span data-ttu-id="c0e32-125">Inicio implícito de la consulta</span><span class="sxs-lookup"><span data-stu-id="c0e32-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="c0e32-126">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="c0e32-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="c0e32-127">Final de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="c0e32-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c0e32-128">D3DDEVINFO \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="c0e32-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="c0e32-129">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="c0e32-129">Retail/Debug</span></span> | <span data-ttu-id="c0e32-130">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="c0e32-130">CreateDevice</span></span>                |
| <span data-ttu-id="c0e32-131">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="c0e32-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="c0e32-132">Final de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="c0e32-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c0e32-133">D3DDEVINFO \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="c0e32-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="c0e32-134">Solo depuración</span><span class="sxs-lookup"><span data-stu-id="c0e32-134">Debug only</span></span>   | <span data-ttu-id="c0e32-135">Presente</span><span class="sxs-lookup"><span data-stu-id="c0e32-135">Present</span></span>                     |
| <span data-ttu-id="c0e32-136">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="c0e32-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="c0e32-137">Final de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="c0e32-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c0e32-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="c0e32-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="c0e32-139">Solo depuración</span><span class="sxs-lookup"><span data-stu-id="c0e32-139">Debug only</span></span>   | <span data-ttu-id="c0e32-140">Presente</span><span class="sxs-lookup"><span data-stu-id="c0e32-140">Present</span></span>                     |
| <span data-ttu-id="c0e32-141">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="c0e32-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="c0e32-142">Final de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="c0e32-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c0e32-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="c0e32-143">BOOL</span></span>                        | <span data-ttu-id="c0e32-144">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="c0e32-144">Retail/Debug</span></span> | <span data-ttu-id="c0e32-145">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="c0e32-145">CreateDevice</span></span>                |
| <span data-ttu-id="c0e32-146">Oclusión de D3DQUERYTYPE \_</span><span class="sxs-lookup"><span data-stu-id="c0e32-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="c0e32-147">D3DISSUE \_ Begin, D3DISSUE \_ End</span><span class="sxs-lookup"><span data-stu-id="c0e32-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="c0e32-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="c0e32-148">DWORD</span></span>                       | <span data-ttu-id="c0e32-149">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="c0e32-149">Retail/Debug</span></span> | <span data-ttu-id="c0e32-150">N/D</span><span class="sxs-lookup"><span data-stu-id="c0e32-150">N/A</span></span>                         |



 

<span data-ttu-id="c0e32-151">Campo Flags para [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="c0e32-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="c0e32-152">Campo Flags para [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="c0e32-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="c0e32-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0e32-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0e32-154">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="c0e32-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
