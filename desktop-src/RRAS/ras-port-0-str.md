---
title: RAS_PORT_0 estructura (rassapi. h)
description: La estructura del puerto de RAS \_ \_ 0 contiene información que describe un puerto ras.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 de la estructura RAS
- PRAS_PORT_0 de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534269"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="7065c-105">\_Estructura del puerto 0 de Ras \_</span><span class="sxs-lookup"><span data-stu-id="7065c-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="7065c-106">\[Esta versión de la estructura del **\_ Puerto \_ 0 de Ras** no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7065c-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="7065c-107">En su lugar, use el [**\_ Puerto ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) más reciente definido en mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="7065c-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="7065c-108">La estructura del **Puerto de Ras \_ \_ 0** contiene información que describe un puerto ras.</span><span class="sxs-lookup"><span data-stu-id="7065c-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="7065c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7065c-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="7065c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7065c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="7065c-111">**wszPortName**</span><span class="sxs-lookup"><span data-stu-id="7065c-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-112">Una cadena Unicode terminada en null que especifica el nombre del puerto, como "COM1".</span><span class="sxs-lookup"><span data-stu-id="7065c-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="7065c-113">**wszDeviceType**</span><span class="sxs-lookup"><span data-stu-id="7065c-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-114">Una cadena Unicode terminada en null que especifica el tipo de dispositivo en el que se realizó la conexión, como módem o ISDN (RDSI).</span><span class="sxs-lookup"><span data-stu-id="7065c-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="7065c-115">La lista de tipos de dispositivos que se pueden especificar en este miembro incluye todos los tipos de dispositivos instalados en el servidor, incluidos los dispositivos de terceros.</span><span class="sxs-lookup"><span data-stu-id="7065c-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-116">**wszDeviceName**</span><span class="sxs-lookup"><span data-stu-id="7065c-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-117">Una cadena Unicode terminada en null que especifica el nombre del dispositivo en el que se realizó la conexión, como "Hayes 9600" o "PCIMACISDN1".</span><span class="sxs-lookup"><span data-stu-id="7065c-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="7065c-118">**wszMediaName**</span><span class="sxs-lookup"><span data-stu-id="7065c-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-119">Especifica una cadena Unicode terminada en null que especifica el nombre del medio utilizado para la conexión, como *Rasser* o *rastapi*.</span><span class="sxs-lookup"><span data-stu-id="7065c-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-120">**sector**</span><span class="sxs-lookup"><span data-stu-id="7065c-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7065c-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-122">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="7065c-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-123">Especifica un conjunto de marcadores de bits que especifican la naturaleza de la conexión realizada en este puerto.</span><span class="sxs-lookup"><span data-stu-id="7065c-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="7065c-124">Este miembro puede ser una combinación de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7065c-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="7065c-125">Value</span><span class="sxs-lookup"><span data-stu-id="7065c-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="7065c-126">Significado</span><span class="sxs-lookup"><span data-stu-id="7065c-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="7065c-127"><dt>**PUERTA de enlace \_ activa**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="7065c-128">Si se establece esta marca, la puerta de enlace NetBIOS está activa en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7065c-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="7065c-129"><dt>**MESSENGER \_ presente**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="7065c-130">Si se establece esta marca, el servicio mensajero se está ejecutando en el cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="7065c-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="7065c-131"><dt>**PUERTO con \_ MULTIvínculo**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="7065c-132">Si se establece esta marca, el puerto está vinculado a otros puertos.</span><span class="sxs-lookup"><span data-stu-id="7065c-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="7065c-133">Use esta información para mostrar el estado de la conexión como un puerto multivínculo.</span><span class="sxs-lookup"><span data-stu-id="7065c-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="7065c-134">En el caso de un puerto multivínculo, la estructura de [**\_ \_ estadísticas del puerto ras**](ras-port-statistics-str.md) contiene dos conjuntos de estadísticas: uno para el puerto independiente y otro para los puertos combinados en la conexión de multivínculo.</span><span class="sxs-lookup"><span data-stu-id="7065c-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="7065c-135"><dt>**\_cliente ppp**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="7065c-136">Si se establece esta marca, el cliente remoto se conecta mediante PPP.</span><span class="sxs-lookup"><span data-stu-id="7065c-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="7065c-137">Si no se establece esta marca, el cliente remoto se conecta mediante el protocolo AMB.</span><span class="sxs-lookup"><span data-stu-id="7065c-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="7065c-138"><dt>**\_escucha remota**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="7065c-139">Si se establece esta marca, el parámetro RemoteListen de la puerta de enlace de NetBIOS se establece en 1 en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7065c-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="7065c-140"><dt>**USUARIO \_ autenticado**</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="7065c-141">Si se establece esta marca, un cliente remoto está conectado al servidor y el usuario se ha autenticado.</span><span class="sxs-lookup"><span data-stu-id="7065c-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="7065c-142">Active esta marca para asegurarse de que un cliente está conectado realmente a un puerto.</span><span class="sxs-lookup"><span data-stu-id="7065c-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="7065c-143">Si \_ están configuradas las marcas Messenger presente, puerta de enlace \_ activa y \_ escucha remota, utilice el servicio mensajero para enviar un mensaje administrativo al cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="7065c-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="7065c-144">Si \_ se establecen Messenger presente y \_ la escucha remota, pero la puerta de enlace \_ activa no, envía mensajes al cliente solo desde el servidor RAS al que está conectado el cliente.</span><span class="sxs-lookup"><span data-stu-id="7065c-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="7065c-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-146">Una cadena Unicode terminada en null que especifica el nombre del usuario remoto conectado a este puerto.</span><span class="sxs-lookup"><span data-stu-id="7065c-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-147">**wszComputer**</span><span class="sxs-lookup"><span data-stu-id="7065c-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-148">Una cadena Unicode terminada en null que especifica el nombre del equipo cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="7065c-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-149">**dwStartSessionTime**</span><span class="sxs-lookup"><span data-stu-id="7065c-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-150">Especifica el tiempo, en segundos desde el 1 de enero de 1970, que el cliente conectó al servidor RAS en este puerto.</span><span class="sxs-lookup"><span data-stu-id="7065c-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="7065c-151">Use las funciones estándar de hora para dar formato a este valor para su presentación.</span><span class="sxs-lookup"><span data-stu-id="7065c-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-152">**wszLogonDomain**</span><span class="sxs-lookup"><span data-stu-id="7065c-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-153">Especifica una cadena Unicode terminada en null que especifica el nombre del dominio en el que se autenticó el usuario remoto.</span><span class="sxs-lookup"><span data-stu-id="7065c-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="7065c-154">Esta cadena es solo el nombre de dominio, sin el \\ \\ prefijo "".</span><span class="sxs-lookup"><span data-stu-id="7065c-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="7065c-155">**fAdvancedServer**</span><span class="sxs-lookup"><span data-stu-id="7065c-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="7065c-156">Especifica una marca que es distinto de cero si el servidor RAS asociado a este puerto es un servidor avanzado, como Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="7065c-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="7065c-157">Utilice esta información para determinar el nombre del servidor que tiene la base de datos de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="7065c-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="7065c-158">Si el servidor RAS es un servidor avanzado, obtenga el nombre del servidor de cuentas de usuario mediante la concatenación del prefijo " \\ \\ " en el nombre devuelto en el miembro **wszLogonDomain** .</span><span class="sxs-lookup"><span data-stu-id="7065c-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="7065c-159">Esto se debe a que para un servidor avanzado, el nombre de dominio de inicio de sesión local es el mismo que el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="7065c-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="7065c-160">Si el servidor RAS es una estación de trabajo, utilice la función [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) para obtener el nombre del servidor de cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="7065c-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7065c-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7065c-161">Requirements</span></span>



| <span data-ttu-id="7065c-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="7065c-162">Requirement</span></span> | <span data-ttu-id="7065c-163">Value</span><span class="sxs-lookup"><span data-stu-id="7065c-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7065c-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7065c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="7065c-165">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7065c-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7065c-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7065c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="7065c-167">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7065c-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7065c-168">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7065c-168">End of client support</span></span><br/>    | <span data-ttu-id="7065c-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7065c-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="7065c-170">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7065c-170">End of server support</span></span><br/>    | <span data-ttu-id="7065c-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7065c-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="7065c-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7065c-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7065c-173"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7065c-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7065c-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="7065c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7065c-175">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="7065c-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7065c-176">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="7065c-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="7065c-177">**\_Puerto ras \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7065c-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="7065c-178">**\_estadísticas de Puerto ras \_**</span><span class="sxs-lookup"><span data-stu-id="7065c-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="7065c-179">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="7065c-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="7065c-180">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="7065c-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





