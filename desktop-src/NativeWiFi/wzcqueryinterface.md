---
description: Proporciona información detallada para una interfaz de LAN inalámbrica administrada por el servicio de configuración inalámbrica rápida.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Función WZCQueryInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912521"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="53f84-103">WZCQueryInterface función)</span><span class="sxs-lookup"><span data-stu-id="53f84-103">WZCQueryInterface function</span></span>

<span data-ttu-id="53f84-104">\[**WZCQueryInterface** ya no es compatible con Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="53f84-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="53f84-105">En su lugar, use la función [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="53f84-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="53f84-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="53f84-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="53f84-107">\]</span><span class="sxs-lookup"><span data-stu-id="53f84-107">\]</span></span>

<span data-ttu-id="53f84-108">La función **WZCQueryInterface** proporciona información detallada para una interfaz de LAN inalámbrica administrada por el servicio de configuración inalámbrica rápida.</span><span class="sxs-lookup"><span data-stu-id="53f84-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="53f84-109">Proporciona información detallada para una interfaz determinada.</span><span class="sxs-lookup"><span data-stu-id="53f84-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f84-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53f84-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="53f84-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53f84-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f84-112">*pSrvAddr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53f84-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f84-113">Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función.</span><span class="sxs-lookup"><span data-stu-id="53f84-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="53f84-114">Si este parámetro es **null**, el servicio de configuración inalámbrica cero se consulta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="53f84-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="53f84-115">Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="53f84-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="53f84-116">*dwInFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="53f84-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f84-117">Los campos que se van a consultar.</span><span class="sxs-lookup"><span data-stu-id="53f84-117">The fields to be queried.</span></span> <span data-ttu-id="53f84-118">Se trata de una máscara de máscara que puede contener cualquier combinación de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="53f84-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="53f84-119">Value</span><span class="sxs-lookup"><span data-stu-id="53f84-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="53f84-120">Significado</span><span class="sxs-lookup"><span data-stu-id="53f84-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="53f84-121"><dt>**Intf \_ DYNFLAGS**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="53f84-122">Devuelve el valor del miembro **dwDynFlags** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="53f84-123"><dt>**Intf \_ DESCr**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="53f84-124">Devuelve el valor del miembro **wszDescr** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="53f84-125"><dt>**Intf \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="53f84-126">Devuelva los valores de los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** en la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="53f84-127"><dt>**Intf \_ PREFLIST**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="53f84-128">Devuelve la lista de redes preferida en el miembro **rdStSSIDList** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="53f84-129"><dt>**Intf \_ CAPACIDADES**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="53f84-130">Devuelva los valores de los miembros **dwCapabilities** y **rdNicCapabilities** en la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="53f84-131"><dt>**Intf \_ INFRAMODE**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="53f84-132">Devuelve el valor del miembro **nInfraMode** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="53f84-133">El miembro **nInfraMode** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="53f84-134"><dt>**Intf \_ AUTHMODE**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="53f84-135">Devuelve el valor del miembro **nAuthMode** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="53f84-136">El miembro **nAuthMode** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="53f84-137"><dt>**Intf \_ WEPSTATUS**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="53f84-138">Devuelve el valor del miembro **nWepStatus** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="53f84-139">El miembro **nWepStatus** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="53f84-140"><dt>**Intf \_ SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="53f84-141">Devuelve el valor del miembro **rdSSID** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="53f84-142">El miembro **rdSSID** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="53f84-143"><dt>**Intf \_ BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="53f84-144">Devuelve el valor del miembro **rdBSSID** en la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="53f84-145">El miembro **rdBSSID** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="53f84-146"><dt>**Intf \_ BSSIDLIST**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="53f84-147">Devuelve la lista visible de redes en el miembro **rdBSSIDList** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="53f84-148">El miembro **rdBSSIDList** solo es válido en algunos Estados de contexto de interfaz.</span><span class="sxs-lookup"><span data-stu-id="53f84-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="53f84-149">*pIntf* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="53f84-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f84-150">En la entrada, puntero a la clave de la interfaz que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="53f84-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="53f84-151">En la salida, puntero a los datos de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="53f84-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="53f84-152">Este parámetro es un puntero a una estructura de [**\_ entrada Intf**](intf-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="53f84-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="53f84-153">*pdwOutFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="53f84-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f84-154">Un conjunto de campos recuperados correctamente.</span><span class="sxs-lookup"><span data-stu-id="53f84-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f84-155">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53f84-155">Return value</span></span>

<span data-ttu-id="53f84-156">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="53f84-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="53f84-157">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="53f84-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="53f84-158">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="53f84-158">Return code</span></span>                                                                                               | <span data-ttu-id="53f84-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="53f84-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53f84-160"><dt>**ERROR de la \_ arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="53f84-161">Los bloques de control de almacenamiento se han destruido.</span><span class="sxs-lookup"><span data-stu-id="53f84-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="53f84-162">Se devuelve este error si el servicio de configuración inalámbrica cero no ha inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="53f84-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="53f84-163"><dt>**\_ \_ no \_ se encontró el archivo de error**</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="53f84-164">El sistema no encuentra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="53f84-164">The system cannot find the file specified.</span></span> <span data-ttu-id="53f84-165">Se devuelve este error si el GUID del miembro **wszGuid** de la estructura [**de \_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* no coincidía con ninguna de las interfaces LAN inalámbricas del equipo local.</span><span class="sxs-lookup"><span data-stu-id="53f84-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="53f84-166"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="53f84-167">Un parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="53f84-167">A parameter is incorrect.</span></span> <span data-ttu-id="53f84-168">Se devuelve este error si el parámetro *pIntf* es **null**.</span><span class="sxs-lookup"><span data-stu-id="53f84-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="53f84-169">Este error se devuelve si el miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* es **null**.</span><span class="sxs-lookup"><span data-stu-id="53f84-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="53f84-170"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="53f84-171">No hay suficiente memoria disponible para procesar esta solicitud y asignar memoria para los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="53f84-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="53f84-172"><dt>**Estado de RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="53f84-173">Varios códigos de error.</span><span class="sxs-lookup"><span data-stu-id="53f84-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="53f84-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53f84-174">Remarks</span></span>

<span data-ttu-id="53f84-175">El miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="53f84-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="53f84-176">Se puede recuperar una lista de interfaces de LAN inalámbrica mediante una llamada a la función [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="53f84-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="53f84-177">Los siguientes miembros de la estructura de [**\_ entrada Intf**](intf-entry.md) a la que apunta *pIntf* deben establecerse en 0 antes de una llamada a la función **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** y **rdCtrlData**.</span><span class="sxs-lookup"><span data-stu-id="53f84-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="53f84-178">El servicio de configuración inalámbrica rápida no automotically actualizar el estado de los medios, incluso cuando se reciben eventos de medios conectados y desconectados.</span><span class="sxs-lookup"><span data-stu-id="53f84-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="53f84-179">Una aplicación debe forzar una actualización del estado de los medios mediante una llamada a la función [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de llamar a la función **WZCQueryInterface** si se va a solicitar el estado de medios NDIS (el \_ bit de Intf NDISMEDIA se establecerá en el parámetro *dwInFlags* ).</span><span class="sxs-lookup"><span data-stu-id="53f84-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="53f84-180">Cuando el parámetro *dwInFlags* contiene **Intf \_ BSSIDLIST**, la función **WZCQueryInterface** no establece *dwOutFlags* con **Intf \_ BSSIDLIST** si la lista de redes visible está vacía.</span><span class="sxs-lookup"><span data-stu-id="53f84-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="53f84-181">Cuando el parámetro *dwInFlags* contiene **Intf \_ SSID**, la función **WZCQueryInterface** no establece *DWOUTFLAGS* con **Intf \_ SSID** si no hay ningún SSID disponible.</span><span class="sxs-lookup"><span data-stu-id="53f84-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="53f84-182">Si la función **WZCQueryInterface** devuelve el error \_ Success, el llamador debe llamar a la función [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) con el parámetro *pIntf* para liberar los búferes internos asignados a los datos devueltos cuando ya no se necesite esta información.</span><span class="sxs-lookup"><span data-stu-id="53f84-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="53f84-183">Esto libera los búferes que usan los miembros **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** y **rdCtrlData** de la estructura [**de \_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="53f84-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="53f84-184">El archivo de encabezado *wzcsapi. h* y el archivo de biblioteca de importación *wzcsapi. lib* no están disponibles en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="53f84-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53f84-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53f84-185">Requirements</span></span>



| <span data-ttu-id="53f84-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f84-186">Requirement</span></span> | <span data-ttu-id="53f84-187">Value</span><span class="sxs-lookup"><span data-stu-id="53f84-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f84-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53f84-188">Minimum supported client</span></span><br/> | <span data-ttu-id="53f84-189">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="53f84-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="53f84-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53f84-190">Minimum supported server</span></span><br/> | <span data-ttu-id="53f84-191">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="53f84-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="53f84-192">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="53f84-192">End of client support</span></span><br/>    | <span data-ttu-id="53f84-193">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="53f84-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="53f84-194">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="53f84-194">End of server support</span></span><br/>    | <span data-ttu-id="53f84-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53f84-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="53f84-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53f84-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f84-197"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="53f84-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53f84-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="53f84-199"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="53f84-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53f84-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53f84-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53f84-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f84-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="53f84-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f84-203">**\_entrada Intf**</span><span class="sxs-lookup"><span data-stu-id="53f84-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="53f84-204">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="53f84-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="53f84-205">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="53f84-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="53f84-206">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="53f84-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
