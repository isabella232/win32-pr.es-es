---
title: RAS_PORT_1 estructura (rassapi. h)
description: La \_ estructura del puerto ras \_ 1 contiene información acerca de un puerto ras.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 de la estructura RAS
- PRAS_PORT_1 de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651398"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="076f6-105">\_Estructura del puerto 1 de Ras \_</span><span class="sxs-lookup"><span data-stu-id="076f6-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="076f6-106">\[Esta versión de la estructura del **\_ Puerto \_ 1 de Ras** no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="076f6-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="076f6-107">En su lugar, use el [**\_ Puerto ras \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) más reciente definido en mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="076f6-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="076f6-108">La estructura del **\_ Puerto ras \_ 1** contiene información acerca de un puerto ras.</span><span class="sxs-lookup"><span data-stu-id="076f6-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="076f6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="076f6-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="076f6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="076f6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="076f6-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="076f6-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-112">Especifica una estructura de [**\_ Puerto \_ 0 de Ras**](ras-port-0-str.md) que contiene información sobre el puerto, como el nombre del puerto, el nombre del usuario remoto conectado al puerto, etc.</span><span class="sxs-lookup"><span data-stu-id="076f6-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="076f6-113">**LineCondition**</span><span class="sxs-lookup"><span data-stu-id="076f6-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-114">Especifica el estado del puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-114">Specifies the state of the port.</span></span> <span data-ttu-id="076f6-115">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="076f6-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="076f6-116">Value</span><span class="sxs-lookup"><span data-stu-id="076f6-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="076f6-117">Significado</span><span class="sxs-lookup"><span data-stu-id="076f6-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="076f6-118"><dt>**\_Puerto ras \_ no \_ operativo**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="076f6-119">El puerto no es operativo.</span><span class="sxs-lookup"><span data-stu-id="076f6-119">The port is not operational.</span></span> <span data-ttu-id="076f6-120">Busque en el registro de eventos los errores detectados por el servidor.</span><span class="sxs-lookup"><span data-stu-id="076f6-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="076f6-121"><dt>**\_Puerto ras \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="076f6-122">El puerto está actualmente desconectado.</span><span class="sxs-lookup"><span data-stu-id="076f6-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="076f6-123"><dt>**\_devolución de \_ llamada del puerto ras \_**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="076f6-124">El servidor RAS está devolviendo al cliente RAS.</span><span class="sxs-lookup"><span data-stu-id="076f6-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="076f6-125"><dt>**\_escucha de Puerto ras \_**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="076f6-126">El puerto está esperando a que un cliente llame a en.</span><span class="sxs-lookup"><span data-stu-id="076f6-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="076f6-127"><dt>**\_autenticación de Puerto ras \_**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="076f6-128">El servidor está en proceso de autenticación del cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="076f6-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="076f6-129"><dt>**\_Puerto ras \_ autenticado**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="076f6-130">El cliente remoto ya está autenticado.</span><span class="sxs-lookup"><span data-stu-id="076f6-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="076f6-131"><dt>**\_inicialización del puerto ras \_**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="076f6-132">El dispositivo conectado al puerto se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="076f6-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="076f6-133">El estado del puerto cambiará al puerto RAS \_ \_ escuchando cuando se haya completado la inicialización.</span><span class="sxs-lookup"><span data-stu-id="076f6-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="076f6-134">**HardwareCondition**</span><span class="sxs-lookup"><span data-stu-id="076f6-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-135">Especifica uno de los siguientes valores para indicar el estado del dispositivo conectado al puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="076f6-136">Value</span><span class="sxs-lookup"><span data-stu-id="076f6-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="076f6-137">Significado</span><span class="sxs-lookup"><span data-stu-id="076f6-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="076f6-138"><dt>**\_módem ras \_ operativo**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="076f6-139">El módem conectado a este puerto está operativo y está listo para recibir llamadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="076f6-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="076f6-140"><dt>**\_error de \_ hardware del módem ras \_**</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="076f6-141">El módem conectado a este puerto tiene un problema de hardware.</span><span class="sxs-lookup"><span data-stu-id="076f6-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="076f6-142">**LineSpeed**</span><span class="sxs-lookup"><span data-stu-id="076f6-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-143">Especifica la velocidad, en bits por segundo, con la que el equipo puede comunicarse con el puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="076f6-144">**NumStatistics**</span><span class="sxs-lookup"><span data-stu-id="076f6-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-145">Este miembro no se usa.</span><span class="sxs-lookup"><span data-stu-id="076f6-145">This member is not used.</span></span> <span data-ttu-id="076f6-146">Las funciones de administración de RAS, como la función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilizan la estructura de [**\_ \_ estadísticas de Puerto ras**](ras-port-statistics-str.md) para devolver estadísticas de puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="076f6-147">**NumMediaParms**</span><span class="sxs-lookup"><span data-stu-id="076f6-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-148">Especifica el número de parámetros específicos del medio para este puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="076f6-149">En el caso de los medios en serie, suele ser el número de valores que aparecen en el archivo de SERIAL.INI.</span><span class="sxs-lookup"><span data-stu-id="076f6-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="076f6-150">**SizeMediaParms**</span><span class="sxs-lookup"><span data-stu-id="076f6-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-151">Especifica el tamaño, en bytes, del búfer necesario para todos los parámetros específicos del medio.</span><span class="sxs-lookup"><span data-stu-id="076f6-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="076f6-152">La función [**RasAdminPortGetInfo**](rasadminportgetinfo.md) devuelve un búfer que contiene una matriz de estructuras de [**\_ parámetros ras**](ras-parameters-str.md) con los valores y parámetros multimedia del puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="076f6-153">**ProjResult**</span><span class="sxs-lookup"><span data-stu-id="076f6-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="076f6-154">Estructura del resultado de la [**\_ \_ proyección \_ PPP de Ras**](ras-ppp-projection-result-str.md) que especifica la información de proyección PPP para este puerto.</span><span class="sxs-lookup"><span data-stu-id="076f6-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="076f6-155">Esta estructura proporciona información para cada protocolo que se negocia cuando un cliente RAS se conecta a un servidor.</span><span class="sxs-lookup"><span data-stu-id="076f6-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="076f6-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076f6-156">Requirements</span></span>



| <span data-ttu-id="076f6-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="076f6-157">Requirement</span></span> | <span data-ttu-id="076f6-158">Value</span><span class="sxs-lookup"><span data-stu-id="076f6-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="076f6-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="076f6-160">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="076f6-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="076f6-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="076f6-162">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="076f6-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="076f6-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="076f6-163">End of client support</span></span><br/>    | <span data-ttu-id="076f6-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="076f6-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="076f6-165">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="076f6-165">End of server support</span></span><br/>    | <span data-ttu-id="076f6-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="076f6-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="076f6-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="076f6-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="076f6-168"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="076f6-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076f6-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="076f6-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076f6-170">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="076f6-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="076f6-171">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="076f6-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="076f6-172">**parámetros de RAS \_**</span><span class="sxs-lookup"><span data-stu-id="076f6-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="076f6-173">**\_Puerto ras \_ 0**</span><span class="sxs-lookup"><span data-stu-id="076f6-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="076f6-174">**\_estadísticas de Puerto ras \_**</span><span class="sxs-lookup"><span data-stu-id="076f6-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="076f6-175">**\_resultado de \_ proyección \_ PPP de Ras**</span><span class="sxs-lookup"><span data-stu-id="076f6-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="076f6-176">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="076f6-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="076f6-177">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="076f6-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="076f6-178">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="076f6-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





