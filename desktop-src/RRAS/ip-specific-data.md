---
title: Estructura de IP_SPECIFIC_DATA (RTM. h)
description: La \_ estructura de datos específica de IP contiene datos específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA de la estructura RAS
- PIP_SPECIFIC_DATA de puntero de estructura RAS
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150618"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="28fc8-105">\_Estructura de datos específica de IP \_</span><span class="sxs-lookup"><span data-stu-id="28fc8-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="28fc8-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="28fc8-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="28fc8-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="28fc8-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="28fc8-108">La estructura de **\_ datos específica de IP** contiene datos específicos de IP.</span><span class="sxs-lookup"><span data-stu-id="28fc8-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fc8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28fc8-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="28fc8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="28fc8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="28fc8-111">**\_Tipo FSD**</span><span class="sxs-lookup"><span data-stu-id="28fc8-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-112">Especifica el tipo de ruta tal y como se define en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="28fc8-113">En la tabla siguiente se muestran los valores posibles para este miembro.</span><span class="sxs-lookup"><span data-stu-id="28fc8-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="28fc8-114">Miembro</span><span class="sxs-lookup"><span data-stu-id="28fc8-114">Member</span></span>                                                                                               | <span data-ttu-id="28fc8-115">Significado</span><span class="sxs-lookup"><span data-stu-id="28fc8-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="28fc8-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="28fc8-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="28fc8-117">No se ha especificado el tipo de ruta.</span><span class="sxs-lookup"><span data-stu-id="28fc8-117">The route type is not specified.</span></span> <span data-ttu-id="28fc8-118">El tipo es diferente del que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="28fc8-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="28fc8-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="28fc8-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="28fc8-120">La ruta no es válida.</span><span class="sxs-lookup"><span data-stu-id="28fc8-120">The route is invalid.</span></span> <span data-ttu-id="28fc8-121">Normalmente, este valor se usa para invalidar una ruta.</span><span class="sxs-lookup"><span data-stu-id="28fc8-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="28fc8-122">Sin embargo, dado que el administrador de tablas de enrutamiento no admite la invalidación, la ruta se sigue considerando en los cálculos de la mejor ruta.</span><span class="sxs-lookup"><span data-stu-id="28fc8-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="28fc8-123">Por lo tanto, los protocolos de enrutamiento no deben usar este valor.</span><span class="sxs-lookup"><span data-stu-id="28fc8-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="28fc8-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="28fc8-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="28fc8-125">La ruta es una ruta local, es decir, el próximo salto es el destino final.</span><span class="sxs-lookup"><span data-stu-id="28fc8-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="28fc8-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="28fc8-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="28fc8-127">La ruta es una ruta remota, es decir, el próximo salto no es el destino final.</span><span class="sxs-lookup"><span data-stu-id="28fc8-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="28fc8-128">**\_Directiva FSD**</span><span class="sxs-lookup"><span data-stu-id="28fc8-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-129">Especifica el conjunto de condiciones que daría lugar a la selección de una ruta de múltiples rutas.</span><span class="sxs-lookup"><span data-stu-id="28fc8-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="28fc8-130">Este miembro está normalmente en formato TOS de IP.</span><span class="sxs-lookup"><span data-stu-id="28fc8-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="28fc8-131">Para obtener más información, consulte [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-132">**FSD \_ NextHopAS**</span><span class="sxs-lookup"><span data-stu-id="28fc8-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-133">Especifica el número de sistema autónomo del próximo salto.</span><span class="sxs-lookup"><span data-stu-id="28fc8-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-134">**Prioridad de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="28fc8-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-135">Especifica un valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="28fc8-135">Specifies a metric value.</span></span> <span data-ttu-id="28fc8-136">El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con las entradas de ruta obtenidas de otros protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="28fc8-137">El valor de este miembro se establece mediante el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-138">**Métrica de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="28fc8-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-139">Especifica un valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="28fc8-139">Specifies a metric value.</span></span> <span data-ttu-id="28fc8-140">El administrador de tablas de enrutamiento usa este valor para comparar esta entrada de ruta con otras entradas de ruta obtenidas del mismo protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="28fc8-141">El valor de este miembro se establece mediante el protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-142">**FSD \_ Metric1**</span><span class="sxs-lookup"><span data-stu-id="28fc8-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-143">Especifica un valor de métrica específico del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="28fc8-144">Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-145">**FSD \_ métrica2**</span><span class="sxs-lookup"><span data-stu-id="28fc8-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-146">Especifica un valor de métrica específico del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="28fc8-147">Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-148">**FSD \_ Metric3**</span><span class="sxs-lookup"><span data-stu-id="28fc8-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-149">Especifica un valor de métrica específico del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="28fc8-150">Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-151">**FSD \_ Metric4**</span><span class="sxs-lookup"><span data-stu-id="28fc8-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-152">Especifica un valor de métrica específico del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="28fc8-153">Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-154">**FSD \_ Metric5**</span><span class="sxs-lookup"><span data-stu-id="28fc8-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-155">Especifica un valor de métrica específico del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="28fc8-156">Este valor de métrica se documenta en [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="28fc8-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc8-157">**Marcas de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="28fc8-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="28fc8-158">Especifica si la ruta es válida.</span><span class="sxs-lookup"><span data-stu-id="28fc8-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="28fc8-159">El protocolo de enrutamiento debe borrar primero estas marcas y, a continuación, establecer la ruta como válida o no válida.</span><span class="sxs-lookup"><span data-stu-id="28fc8-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="28fc8-160">El protocolo de enrutamiento debe usar las macros **ClearRouteFlags ()**, **SetRouteValid ()** y **ClearRouteValid ()** para realizar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="28fc8-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="28fc8-161">Estas macros se definen en RTM. h.</span><span class="sxs-lookup"><span data-stu-id="28fc8-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28fc8-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28fc8-162">Remarks</span></span>

<span data-ttu-id="28fc8-163">El administrador de tablas de enrutamiento usa los miembros **FSD \_ Priority** y **FSD \_ Metric** para calcular la mejor ruta a una red de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="28fc8-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="28fc8-164">Los **miembros \_ \[ 1-5 \]** de la métrica de FSD son para la conformidad con la MIB II.</span><span class="sxs-lookup"><span data-stu-id="28fc8-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="28fc8-165">Los agentes MIB II solo muestran estos valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="28fc8-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="28fc8-166">No muestran el valor de **métrica \_ FSD** .</span><span class="sxs-lookup"><span data-stu-id="28fc8-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="28fc8-167">Para que se muestre la **\_ métrica FSD** , el protocolo de enrutamiento también debe almacenar el valor en uno de los miembros **FSD \_ Metric \[ 1-5 \]** .</span><span class="sxs-lookup"><span data-stu-id="28fc8-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="28fc8-168">El administrador de tablas de enrutamiento no usa los valores de métricas de los miembros de la **métrica de FSD \_ \[ 1-5 \]** al calcular la mejor ruta a una red de destino.</span><span class="sxs-lookup"><span data-stu-id="28fc8-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="28fc8-169">Por lo tanto, el protocolo de enrutamiento debe asegurarse de que el miembro de **\_ métrica FSD** tenga un valor de métrica adecuado.</span><span class="sxs-lookup"><span data-stu-id="28fc8-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="28fc8-170">Un protocolo de enrutamiento podría usar **las \_ marcas FSD** para marcar una ruta como no válida, si no se debe usar en otros protocolos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="28fc8-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fc8-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28fc8-171">Requirements</span></span>



| <span data-ttu-id="28fc8-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="28fc8-172">Requirement</span></span> | <span data-ttu-id="28fc8-173">Value</span><span class="sxs-lookup"><span data-stu-id="28fc8-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28fc8-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28fc8-174">Minimum supported client</span></span><br/> | <span data-ttu-id="28fc8-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28fc8-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="28fc8-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28fc8-176">Minimum supported server</span></span><br/> | <span data-ttu-id="28fc8-177">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28fc8-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28fc8-178">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="28fc8-178">End of server support</span></span><br/>    | <span data-ttu-id="28fc8-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28fc8-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="28fc8-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28fc8-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="28fc8-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="28fc8-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fc8-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="28fc8-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fc8-183">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="28fc8-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="28fc8-184">Estructuras de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="28fc8-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="28fc8-185">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="28fc8-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





