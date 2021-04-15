---
title: RAS_PORT_STATISTICS estructura (rassapi. h)
description: La \_ estructura de estadísticas del puerto ras informa de \_ las estadísticas que un servidor RAS recopila para un puerto conectado.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS de la estructura RAS
- PRAS_PORT_STATISTICS de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676773"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="e1990-105">Estructura de estadísticas del \_ Puerto ras \_</span><span class="sxs-lookup"><span data-stu-id="e1990-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="e1990-106">\[La estructura de **\_ \_ estadísticas del puerto ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="e1990-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="e1990-107">La estructura de **\_ \_ estadísticas del puerto ras** informa de las estadísticas que un servidor RAS recopila para un puerto conectado.</span><span class="sxs-lookup"><span data-stu-id="e1990-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="e1990-108">El servidor RAS restablece los diversos contadores de estadísticas cada vez que se conecta el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="e1990-109">Llame a la función [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para obligar al servidor RAS a restablecer los contadores estadísticos.</span><span class="sxs-lookup"><span data-stu-id="e1990-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="e1990-110">En el caso de un puerto que forme parte de una conexión multivínculo, esta estructura proporciona dos conjuntos de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="e1990-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="e1990-111">El primer conjunto contiene las Estadísticas acumulativas para todos los puertos de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="e1990-112">Estas estadísticas son las mismas para todos los puertos de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="e1990-113">El segundo conjunto contiene las estadísticas de solo este puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="e1990-114">Si el puerto no forma parte de una conexión de multivínculo, ambos conjuntos de estadísticas tienen la misma información.</span><span class="sxs-lookup"><span data-stu-id="e1990-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="e1990-115">Para determinar si un puerto forma parte de una conexión de multivínculo, compruebe el \_ bit MULTIlinked del puerto en el miembro **Flags** de la estructura del puerto ras del puerto. [**\_ \_**](ras-port-0-str.md)</span><span class="sxs-lookup"><span data-stu-id="e1990-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1990-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1990-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="e1990-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1990-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1990-118">**dwBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="e1990-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-119">Especifica el número total de bytes transmitidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-120">**dwBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="e1990-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-121">Especifica el número total de bytes recibidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-122">**dwFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="e1990-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-123">Especifica el número total de fotogramas transmitidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-124">**dwFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="e1990-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-125">Especifica el número total de fotogramas recibidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-126">**dwCrcErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-127">Especifica el número total de errores de CRC en la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="e1990-128">Los errores de CRC se deben a un error en una comprobación de redundancia cíclica.</span><span class="sxs-lookup"><span data-stu-id="e1990-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="e1990-129">Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se detectaron inalterados al llegar.</span><span class="sxs-lookup"><span data-stu-id="e1990-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-130">**dwTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-131">Especifica el número total de errores de tiempo de espera en la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="e1990-132">Los errores de tiempo de espera se producen cuando no se recibe un carácter esperado en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="e1990-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="e1990-133">Cuando esto ocurre, el software presupone que los datos se han perdido y solicita que se reenvíen.</span><span class="sxs-lookup"><span data-stu-id="e1990-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-134">**dwAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-135">Especifica el número total de errores de alineación en la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="e1990-136">Los errores de alineación se producen cuando un carácter recibido no es el esperado.</span><span class="sxs-lookup"><span data-stu-id="e1990-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="e1990-137">Esto suele suceder cuando se pierde un carácter o cuando se produce un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e1990-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-138">**dwHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-139">Especifica el número total de errores de saturación de hardware en la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="e1990-140">Estos errores indican el número de veces que el equipo emisor ha transmitido caracteres más rápido que el equipo receptor puede procesarlos.</span><span class="sxs-lookup"><span data-stu-id="e1990-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="e1990-141">Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.</span><span class="sxs-lookup"><span data-stu-id="e1990-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-142">**dwFramingErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-143">Especifica el número total de errores de tramas de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="e1990-144">Se produce un error de tramas cuando se recibe un carácter asincrónico con un bit de inicio o detención no válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-145">**dwBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-146">Especifica el número total de errores de saturación del búfer en la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="e1990-147">Se produce un error de saturación del búfer cuando el equipo emisor está transmitiendo caracteres más rápido que el equipo receptor.</span><span class="sxs-lookup"><span data-stu-id="e1990-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="e1990-148">Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.</span><span class="sxs-lookup"><span data-stu-id="e1990-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-149">**dwBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-150">Especifica el número total de bytes transmitidos sin comprimir por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-151">**dwBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-152">Especifica el número total de bytes recibidos sin comprimir por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-153">**dwBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-154">Especifica el número total de bytes transmitidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-155">**dwBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-156">Especifica el número total de bytes recibidos comprimidos por la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-157">**dwPortBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="e1990-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-158">Especifica el número total de bytes transmitidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-159">**dwPortBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="e1990-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-160">Especifica el número total de bytes recibidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-161">**dwPortFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="e1990-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-162">Especifica el número total de fotogramas transmitidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-163">**dwPortFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="e1990-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-164">Especifica el número total de fotogramas recibidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-165">**dwPortCrcErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-166">Especifica el número total de errores de CRC en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="e1990-167">Los errores de CRC se deben a un error en una comprobación de redundancia cíclica.</span><span class="sxs-lookup"><span data-stu-id="e1990-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="e1990-168">Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se detectaron inalterados al llegar.</span><span class="sxs-lookup"><span data-stu-id="e1990-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-169">**dwPortTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-170">Especifica el número total de errores de tiempo de espera en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="e1990-171">Los errores de tiempo de espera se producen cuando no se recibe un carácter esperado en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="e1990-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="e1990-172">Cuando esto ocurre, el software presupone que los datos se han perdido y solicita que se reenvíen.</span><span class="sxs-lookup"><span data-stu-id="e1990-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-173">**dwPortAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-174">Especifica el número total de errores de alineación en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="e1990-175">Los errores de alineación se producen cuando un carácter recibido no es el esperado.</span><span class="sxs-lookup"><span data-stu-id="e1990-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="e1990-176">Esto suele suceder cuando se pierde un carácter o cuando se produce un error de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e1990-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-177">**dwPortHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-178">Especifica el número total de errores de saturación de hardware en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="e1990-179">Estos errores indican el número de veces que el equipo emisor ha transmitido caracteres más rápido que el equipo receptor puede procesarlos.</span><span class="sxs-lookup"><span data-stu-id="e1990-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="e1990-180">Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.</span><span class="sxs-lookup"><span data-stu-id="e1990-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-181">**dwPortFramingErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-182">Especifica el número total de errores de tramas en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="e1990-183">Se produce un error de tramas cuando se recibe un carácter asincrónico con un bit de inicio o detención no válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-184">**dwPortBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="e1990-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-185">Especifica el número total de errores de saturación del búfer en el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="e1990-186">Se produce un error de saturación del búfer cuando el equipo emisor está transmitiendo caracteres más rápido que el equipo receptor.</span><span class="sxs-lookup"><span data-stu-id="e1990-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="e1990-187">Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.</span><span class="sxs-lookup"><span data-stu-id="e1990-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-188">**dwPortBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-189">Especifica el número total de bytes transmitidos sin comprimir por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="e1990-190">Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="e1990-191">En su lugar, use las estadísticas de compresión de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-192">**dwPortBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-193">Especifica el número total de bytes recibidos sin comprimir por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="e1990-194">Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="e1990-195">En su lugar, use las estadísticas de compresión de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-196">**dwPortBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-197">Especifica el número total de bytes transmitidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="e1990-198">Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="e1990-199">En su lugar, use las estadísticas de compresión de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="e1990-200">**dwPortBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="e1990-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="e1990-201">Especifica el número total de bytes recibidos comprimidos por el puerto.</span><span class="sxs-lookup"><span data-stu-id="e1990-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="e1990-202">Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1990-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="e1990-203">En su lugar, use las estadísticas de compresión de la conexión.</span><span class="sxs-lookup"><span data-stu-id="e1990-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1990-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1990-204">Requirements</span></span>



| <span data-ttu-id="e1990-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1990-205">Requirement</span></span> | <span data-ttu-id="e1990-206">Value</span><span class="sxs-lookup"><span data-stu-id="e1990-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e1990-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1990-207">Minimum supported client</span></span><br/> | <span data-ttu-id="e1990-208">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1990-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e1990-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1990-209">Minimum supported server</span></span><br/> | <span data-ttu-id="e1990-210">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e1990-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e1990-211">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e1990-211">End of client support</span></span><br/>    | <span data-ttu-id="e1990-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1990-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="e1990-213">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e1990-213">End of server support</span></span><br/>    | <span data-ttu-id="e1990-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e1990-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="e1990-215">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1990-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1990-216"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1990-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1990-217">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1990-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1990-218">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="e1990-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e1990-219">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="e1990-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="e1990-220">**\_Puerto ras \_ 0**</span><span class="sxs-lookup"><span data-stu-id="e1990-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="e1990-221">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="e1990-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="e1990-222">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="e1990-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="e1990-223">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="e1990-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="e1990-224">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e1990-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





