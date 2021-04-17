---
title: Estructura de ORPC_DBG_BUFFER
description: La \_ \_ estructura de búfer ORPC dbg es el formato de búfer utilizado para calcular las referencias de los datos RPC a los métodos de la interfaz IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- Estructura de ORPC_DBG_BUFFER COM
- PORPC_DBG_BUFFER puntero de estructura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695889"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="47eff-105">ORPC \_ \_ estructura de búfer dbg</span><span class="sxs-lookup"><span data-stu-id="47eff-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="47eff-106">La estructura de **\_ \_ búfer ORPC dbg** es el formato de búfer utilizado para calcular las referencias de los datos RPC a los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="47eff-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="47eff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47eff-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="47eff-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="47eff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="47eff-109">**alwaysOrSometimes**</span><span class="sxs-lookup"><span data-stu-id="47eff-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-110">Valor que controla la generación del depurador.</span><span class="sxs-lookup"><span data-stu-id="47eff-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="47eff-111">**alwaysOrSometimes** puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="47eff-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="47eff-112">Value</span><span class="sxs-lookup"><span data-stu-id="47eff-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="47eff-113">Significado</span><span class="sxs-lookup"><span data-stu-id="47eff-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="47eff-114"><dt>**ORPC \_ Depurar \_ siempre**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="47eff-115">Si se establece, COM siempre generará la notificación de cliente o servidor en el receptor.</span><span class="sxs-lookup"><span data-stu-id="47eff-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="47eff-116"><dt>**ORPC \_ Depurar \_ si el \_ enlace \_ está habilitado**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="47eff-117">Si se establece, COM solo generará la notificación de cliente o de servidor en el receptor si se ha habilitado la depuración de COM mediante una llamada a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) en ese proceso con **FTrace** establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="47eff-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="47eff-118">**verMajor**</span><span class="sxs-lookup"><span data-stu-id="47eff-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-119">Número de versión principal de la especificación de formato de datos.</span><span class="sxs-lookup"><span data-stu-id="47eff-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-120">**verMinor**</span><span class="sxs-lookup"><span data-stu-id="47eff-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-121">Número de versión secundaria de la especificación de formato de datos.</span><span class="sxs-lookup"><span data-stu-id="47eff-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-122">**cbRemaining**</span><span class="sxs-lookup"><span data-stu-id="47eff-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-123">El número de bytes, incluido **cbRemaining**, que siguen en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="47eff-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-124">**guidSemantic**</span><span class="sxs-lookup"><span data-stu-id="47eff-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-125">Un GUID que determina qué miembros de la Unión están presentes a continuación.</span><span class="sxs-lookup"><span data-stu-id="47eff-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="47eff-126">**guidSemantic** puede tomar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="47eff-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="47eff-127">Value</span><span class="sxs-lookup"><span data-stu-id="47eff-127">Value</span></span>                                                                                                           | <span data-ttu-id="47eff-128">Significado</span><span class="sxs-lookup"><span data-stu-id="47eff-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47eff-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="47eff-130">Determina si el depurador realiza una ejecución paso a paso.</span><span class="sxs-lookup"><span data-stu-id="47eff-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="47eff-131">A continuación solo está presente el miembro **fStopOnOtherSide** de la Unión.</span><span class="sxs-lookup"><span data-stu-id="47eff-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="47eff-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="47eff-133">Determina si los datos de serialización RPC y los códigos de la depuración se pasan al receptor.</span><span class="sxs-lookup"><span data-stu-id="47eff-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="47eff-134">Todos los miembros de la Unión están presentes a continuación con la excepción de **fStopOnOtherSide**.</span><span class="sxs-lookup"><span data-stu-id="47eff-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="47eff-135">**fStopOnOtherSide**</span><span class="sxs-lookup"><span data-stu-id="47eff-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-136">Si es **true**, el depurador realiza una ejecución paso a paso y debe salir del servidor y continuar la ejecución una vez que se alcanza el otro lado.</span><span class="sxs-lookup"><span data-stu-id="47eff-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="47eff-137">De lo contrario, no se realiza una ejecución paso a paso y la ejecución del depurador se detiene en el otro lado.</span><span class="sxs-lookup"><span data-stu-id="47eff-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-138">**wDebuggingOpCode**</span><span class="sxs-lookup"><span data-stu-id="47eff-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-139">Un valor que permite especificar una serie de operaciones.</span><span class="sxs-lookup"><span data-stu-id="47eff-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="47eff-140">**wDebuggingOpCode** puede tomar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="47eff-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="47eff-141">Value</span><span class="sxs-lookup"><span data-stu-id="47eff-141">Value</span></span>                                                                             | <span data-ttu-id="47eff-142">Significado</span><span class="sxs-lookup"><span data-stu-id="47eff-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47eff-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="47eff-144">No hay ninguna operación.</span><span class="sxs-lookup"><span data-stu-id="47eff-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="47eff-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="47eff-146">Si se establece, la semántica de un solo paso es idéntica a **fStopOnOtherSide** cuando se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="47eff-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="47eff-147">**cExtent**</span><span class="sxs-lookup"><span data-stu-id="47eff-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-148">Acolcha.</span><span class="sxs-lookup"><span data-stu-id="47eff-148">Padding.</span></span> <span data-ttu-id="47eff-149">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="47eff-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="47eff-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-151">Acolcha.</span><span class="sxs-lookup"><span data-stu-id="47eff-151">Padding.</span></span> <span data-ttu-id="47eff-152">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="47eff-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-153">**CB**</span><span class="sxs-lookup"><span data-stu-id="47eff-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-154">Tamaño, en bytes, de los datos de **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="47eff-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="47eff-155">**guidExtent**</span><span class="sxs-lookup"><span data-stu-id="47eff-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-156">Un **GUID** que determina el tipo de datos en **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="47eff-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="47eff-157">**guidExtent** puede tomar uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="47eff-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="47eff-158">Value</span><span class="sxs-lookup"><span data-stu-id="47eff-158">Value</span></span>                                                                                                           | <span data-ttu-id="47eff-159">Significado</span><span class="sxs-lookup"><span data-stu-id="47eff-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="47eff-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="47eff-161">**rgbData** es un puntero de interfaz de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="47eff-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="47eff-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="47eff-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="47eff-163">Búfer de **bytes** que se usa para pasar datos com de cálculo de referencias RPC entre los depuradores de cliente y de servidor.</span><span class="sxs-lookup"><span data-stu-id="47eff-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="47eff-164">El contenido de **rgbData** viene determinado por el **GUID** de **guidExtent**.</span><span class="sxs-lookup"><span data-stu-id="47eff-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="47eff-165">Valor guidExtent</span><span class="sxs-lookup"><span data-stu-id="47eff-165">guidExtent Value</span></span>                     | <span data-ttu-id="47eff-166">contenido de rgbData</span><span class="sxs-lookup"><span data-stu-id="47eff-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47eff-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="47eff-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="47eff-168">Puntero de interfaz de cálculo de referencias que es el resultado de llamar a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="47eff-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="47eff-169">El puntero de cálculo de referencias se convierte en su puntero de interfaz correspondiente mediante [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="47eff-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47eff-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47eff-170">Remarks</span></span>

<span data-ttu-id="47eff-171">Estos miembros de esta estructura tienen una alineación de 1 byte y se transmiten siempre en orden de bytes Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="47eff-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="47eff-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47eff-172">Requirements</span></span>



| <span data-ttu-id="47eff-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="47eff-173">Requirement</span></span> | <span data-ttu-id="47eff-174">Value</span><span class="sxs-lookup"><span data-stu-id="47eff-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="47eff-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47eff-175">Minimum supported client</span></span><br/> | <span data-ttu-id="47eff-176">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="47eff-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="47eff-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47eff-177">Minimum supported server</span></span><br/> | <span data-ttu-id="47eff-178">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47eff-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="47eff-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47eff-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="47eff-180"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="47eff-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47eff-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="47eff-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47eff-182">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="47eff-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="47eff-183">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="47eff-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="47eff-184">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="47eff-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="47eff-185">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="47eff-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





