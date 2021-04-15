---
title: Valores de configuración
description: El comportamiento de la API del punto de control y la API del host del dispositivo se puede modificar cambiando la configuración del registro.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695256"
---
# <a name="configuration-settings"></a><span data-ttu-id="f8de8-103">Valores de configuración</span><span class="sxs-lookup"><span data-stu-id="f8de8-103">Configuration Settings</span></span>

<span data-ttu-id="f8de8-104">El comportamiento de la [API del punto de control](control-point-api.md) y la [API del host del dispositivo](device-host-api.md) se puede modificar cambiando la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="f8de8-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="f8de8-105">Hay siete valores del registro que afectan al comportamiento:</span><span class="sxs-lookup"><span data-stu-id="f8de8-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="f8de8-106">**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-106">**DownloadScope**</span></span>
-   <span data-ttu-id="f8de8-107">**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="f8de8-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="f8de8-108">\\Host de dispositivo **UPnP** \\ **Límite de tamaño de archivo**</span><span class="sxs-lookup"><span data-stu-id="f8de8-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="f8de8-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Límite de tamaño de archivo**</span><span class="sxs-lookup"><span data-stu-id="f8de8-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="f8de8-110">**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="f8de8-110">**MaxCache**</span></span>
-   <span data-ttu-id="f8de8-111">**TTL**</span><span class="sxs-lookup"><span data-stu-id="f8de8-111">**TTL**</span></span>
-   <span data-ttu-id="f8de8-112">**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-112">**ReceiveScope**</span></span>

<span data-ttu-id="f8de8-113">Hay dos valores de registro denominados **límite de tamaño de archivo**, uno para los documentos de Descripción y el otro para las respuestas que utilizan el Protocolo simple de acceso a objetos (SOAP).</span><span class="sxs-lookup"><span data-stu-id="f8de8-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="f8de8-114">La ubicación de cada uno de los siete valores del registro es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="f8de8-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="f8de8-115">Descripciones de valores del registro</span><span class="sxs-lookup"><span data-stu-id="f8de8-115">Registry Value Descriptions</span></span>

<span data-ttu-id="f8de8-116">Los valores del registro se explican en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="f8de8-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="f8de8-117">Cada valor del registro es **una \_ DWORD** de tipo REG (un entero de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="f8de8-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="f8de8-118">El efecto de cada valor es global.</span><span class="sxs-lookup"><span data-stu-id="f8de8-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="f8de8-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-120">Especifica las direcciones IP válidas para la dirección URL del documento de Descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8de8-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="f8de8-121">Si la dirección IP del host que se especifica en la dirección URL del documento de descripción no está dentro del ámbito especificado por **DownloadScope**, esa dirección IP no es válida y el objeto de dispositivo no se creará.</span><span class="sxs-lookup"><span data-stu-id="f8de8-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="f8de8-122">En la tabla siguiente se muestran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="f8de8-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="f8de8-123">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="f8de8-123">The default value is 1.</span></span>



| <span data-ttu-id="f8de8-124">Valor de **DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="f8de8-125">Significado</span><span class="sxs-lookup"><span data-stu-id="f8de8-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8de8-126">0</span><span class="sxs-lookup"><span data-stu-id="f8de8-126">0</span></span>                          | <span data-ttu-id="f8de8-127">La dirección IP del host debe ser una dirección de subred.</span><span class="sxs-lookup"><span data-stu-id="f8de8-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="f8de8-128">1</span><span class="sxs-lookup"><span data-stu-id="f8de8-128">1</span></span>                          | <span data-ttu-id="f8de8-129">La dirección IP del host debe ser una dirección de subred o una dirección privada que sea de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (según se especifica en RFC 1918) o 169,254. *x*. *x* (según se especifica en RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="f8de8-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="f8de8-130">2</span><span class="sxs-lookup"><span data-stu-id="f8de8-130">2</span></span>                          | <span data-ttu-id="f8de8-131">La dirección IP del host debe ser una dirección de subred, una dirección privada o una dirección que se encuentre dentro de los saltos del período de vida (TTL) desde el punto de control.</span><span class="sxs-lookup"><span data-stu-id="f8de8-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="f8de8-132">3</span><span class="sxs-lookup"><span data-stu-id="f8de8-132">3</span></span>                          | <span data-ttu-id="f8de8-133">La dirección IP del host puede ser cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="f8de8-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="f8de8-134">>3</span><span class="sxs-lookup"><span data-stu-id="f8de8-134">>3</span></span>                      | <span data-ttu-id="f8de8-135">Igual que para el valor 0.</span><span class="sxs-lookup"><span data-stu-id="f8de8-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="f8de8-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="f8de8-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f8de8-137">Optional.</span></span> <span data-ttu-id="f8de8-138">Especifica la duración de un dispositivo, en segundos, que invalida el valor proporcionado en el mensaje del anuncio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8de8-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="f8de8-139">Si **DeviceLifeTime** está presente, se omite el valor especificado en el anuncio del dispositivo y, en su lugar, se usa el valor del registro.</span><span class="sxs-lookup"><span data-stu-id="f8de8-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="f8de8-140">Esto se aplica a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f8de8-140">This applies to all devices.</span></span>

<span data-ttu-id="f8de8-141">Los valores válidos van de 900 a **\_ DWORD máx**.</span><span class="sxs-lookup"><span data-stu-id="f8de8-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="f8de8-142">El valor predeterminado es 1800.</span><span class="sxs-lookup"><span data-stu-id="f8de8-142">The default value is 1800.</span></span> <span data-ttu-id="f8de8-143">Si **DeviceLifeTime** se establece en 0, se usa el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f8de8-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="f8de8-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Host de dispositivo **UPnP** \\ **Límite de tamaño de archivo**</span><span class="sxs-lookup"><span data-stu-id="f8de8-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-145">Especifica el tamaño máximo, en bytes, de cada documento de descripción.</span><span class="sxs-lookup"><span data-stu-id="f8de8-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="f8de8-146">Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="f8de8-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="f8de8-147">En las versiones anteriores, esta configuración se codifica de forma rígida como 102400.</span><span class="sxs-lookup"><span data-stu-id="f8de8-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="f8de8-148">Los valores válidos van de 10240 a **\_ DWORD máx**.</span><span class="sxs-lookup"><span data-stu-id="f8de8-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="f8de8-149">El valor predeterminado es 102400.</span><span class="sxs-lookup"><span data-stu-id="f8de8-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="f8de8-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Límite de tamaño de archivo**</span><span class="sxs-lookup"><span data-stu-id="f8de8-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-151">Especifica el tamaño máximo, en bytes, de la respuesta SOAP que es aceptable.</span><span class="sxs-lookup"><span data-stu-id="f8de8-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="f8de8-152">Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="f8de8-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="f8de8-153">En las versiones anteriores, esta configuración se codifica de forma rígida como 102400.</span><span class="sxs-lookup"><span data-stu-id="f8de8-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="f8de8-154">Los valores válidos van de 10240 a **\_ DWORD máx**.</span><span class="sxs-lookup"><span data-stu-id="f8de8-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="f8de8-155">El valor predeterminado es 102400.</span><span class="sxs-lookup"><span data-stu-id="f8de8-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="f8de8-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="f8de8-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-157">Especifica el número máximo de entradas permitidas en la memoria caché del Protocolo simple de detección de servicios (SSDP).</span><span class="sxs-lookup"><span data-stu-id="f8de8-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="f8de8-158">Los valores válidos oscilan entre 10 y 30000.</span><span class="sxs-lookup"><span data-stu-id="f8de8-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="f8de8-159">El valor predeterminado es 1000.</span><span class="sxs-lookup"><span data-stu-id="f8de8-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="f8de8-160"><span id="TTL"></span><span id="ttl"></span>**PERÍODO**</span><span class="sxs-lookup"><span data-stu-id="f8de8-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-161">Especifica el período de vida de un paquete SSDP.</span><span class="sxs-lookup"><span data-stu-id="f8de8-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="f8de8-162">Es decir, **TTL** especifica el número de saltos permitido para un paquete.</span><span class="sxs-lookup"><span data-stu-id="f8de8-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="f8de8-163">Los valores válidos oscilan entre 1 y 255.</span><span class="sxs-lookup"><span data-stu-id="f8de8-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="f8de8-164">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="f8de8-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8de8-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="f8de8-166">Especifica las direcciones IP que son orígenes válidos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f8de8-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="f8de8-167">Si un mensaje entrante se origina en una dirección que no está dentro del ámbito especificado por **ReceiveScope**, se omite el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f8de8-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="f8de8-168">Esta opción no se puede configurar en las versiones de Windows anteriores a Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="f8de8-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="f8de8-169">En las versiones anteriores, se acepta un mensaje sin tener en cuenta su origen.</span><span class="sxs-lookup"><span data-stu-id="f8de8-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="f8de8-170">En la tabla siguiente se muestran los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="f8de8-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="f8de8-171">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="f8de8-171">The default value is 1.</span></span>



| <span data-ttu-id="f8de8-172">Valor de **ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="f8de8-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="f8de8-173">Significado</span><span class="sxs-lookup"><span data-stu-id="f8de8-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8de8-174">0</span><span class="sxs-lookup"><span data-stu-id="f8de8-174">0</span></span>                         | <span data-ttu-id="f8de8-175">La dirección IP del remitente debe ser una dirección de subred.</span><span class="sxs-lookup"><span data-stu-id="f8de8-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="f8de8-176">1</span><span class="sxs-lookup"><span data-stu-id="f8de8-176">1</span></span>                         | <span data-ttu-id="f8de8-177">La dirección IP del remitente debe ser una dirección de subred o una dirección privada que sea de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (según se especifica en RFC 1918) o 169,254. *x*. *x* (según se especifica en RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="f8de8-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="f8de8-178">2</span><span class="sxs-lookup"><span data-stu-id="f8de8-178">2</span></span>                         | <span data-ttu-id="f8de8-179">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f8de8-179">Not used.</span></span> <span data-ttu-id="f8de8-180">Si **ReceiveScope** se establece en 2, se utiliza el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f8de8-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="f8de8-181">3</span><span class="sxs-lookup"><span data-stu-id="f8de8-181">3</span></span>                         | <span data-ttu-id="f8de8-182">La dirección IP del remitente puede ser cualquier dirección.</span><span class="sxs-lookup"><span data-stu-id="f8de8-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f8de8-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8de8-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8de8-184">Información general sobre la arquitectura de UPnP</span><span class="sxs-lookup"><span data-stu-id="f8de8-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




