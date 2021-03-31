---
description: Actualiza la información de interfaz para una interfaz LAN inalámbrica específica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Función WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361221"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="e261b-103">WZCRefreshInterface función)</span><span class="sxs-lookup"><span data-stu-id="e261b-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="e261b-104">\[**WZCRefreshInterface** no es compatible con Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e261b-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e261b-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="e261b-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="e261b-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="e261b-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="e261b-107">La función **WZCRefreshInterface** actualiza la información de interfaz para una interfaz LAN inalámbrica específica.</span><span class="sxs-lookup"><span data-stu-id="e261b-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e261b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e261b-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e261b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e261b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e261b-110">*pSrvAddr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e261b-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e261b-111">Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función.</span><span class="sxs-lookup"><span data-stu-id="e261b-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="e261b-112">Si este parámetro es **null**, se llama al servicio de configuración inalámbrica cero en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e261b-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="e261b-113">Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="e261b-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="e261b-114">*dwInFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e261b-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e261b-115">Conjunto de campos que se van a actualizar junto con acciones de actualización específicas que se van a realizar.</span><span class="sxs-lookup"><span data-stu-id="e261b-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="e261b-116">Se trata de una máscara de máscara que puede contener cualquier combinación de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e261b-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="e261b-117">Value</span><span class="sxs-lookup"><span data-stu-id="e261b-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="e261b-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e261b-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="e261b-119"><dt>**Intf \_ DESCr**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="e261b-120">Actualice la descripción de la interfaz de una interfaz LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e261b-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="e261b-121">La descripción de la interfaz actualizada se puede recuperar mediante una llamada a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el bit **\_ Descr de Intf** establecido en el parámetro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="e261b-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="e261b-122">La descripción de la interfaz se devuelve en el miembro **wszDescr** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *PIntf* devuelto por la función **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e261b-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="e261b-123"><dt>**Intf \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="e261b-124">Actualice la información multimedia de NDIS para una interfaz de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e261b-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="e261b-125">La información multimedia de NDIS actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) con el conjunto de bits **Intf \_ NDISMEDIA** en el parámetro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="e261b-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="e261b-126">La información multimedia de NDIS se devuelve en los miembros **ulMediaState**, **ulMediaType** y **ulPhysicalMediaType** de la estructura de [**\_ entrada Intf**](intf-entry.md) señalada por el parámetro *pIntf* devuelto por la función **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e261b-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="e261b-127"><dt>**Intf \_ Todos los \_ OID**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="e261b-128">Actualice todos los OID de NDIS para una interfaz de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e261b-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="e261b-129">Esta opción actualiza la mayoría de los datos de una interfaz LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e261b-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="e261b-130">La información actualizada se puede recuperar llamando a la función [**WZCQueryInterface**](wzcqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="e261b-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="e261b-131">*pIntf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e261b-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e261b-132">Puntero a una estructura [**de \_ entrada Intf**](intf-entry.md) que contiene la clave de la interfaz que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="e261b-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="e261b-133">*pdwOutFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e261b-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e261b-134">Un conjunto de campos que se actualizaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="e261b-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e261b-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e261b-135">Return value</span></span>

<span data-ttu-id="e261b-136">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e261b-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e261b-137">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e261b-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="e261b-138">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e261b-138">Return code</span></span>                                                                                              | <span data-ttu-id="e261b-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="e261b-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e261b-140"><dt>**ERROR de la \_ arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="e261b-141">Los bloques de control de almacenamiento se han destruido.</span><span class="sxs-lookup"><span data-stu-id="e261b-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="e261b-142">Se devuelve este error si el servicio de configuración inalámbrica cero no ha inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="e261b-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="e261b-143"><dt>**\_ \_ no \_ se encontró el archivo de error**</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="e261b-144">El sistema no encuentra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e261b-144">The system cannot find the file specified.</span></span> <span data-ttu-id="e261b-145">Se devuelve este error si el GUID del miembro **wszGuid** de la estructura [**de \_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* no coincidía con ninguna de las interfaces LAN inalámbricas del equipo local.</span><span class="sxs-lookup"><span data-stu-id="e261b-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="e261b-146"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="e261b-147">Un parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="e261b-147">A parameter is incorrect.</span></span> <span data-ttu-id="e261b-148">Se devuelve este error si el parámetro *pIntf* es **null**.</span><span class="sxs-lookup"><span data-stu-id="e261b-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="e261b-149">Este error se devuelve si el miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* es **null**.</span><span class="sxs-lookup"><span data-stu-id="e261b-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="e261b-150"><dt>**Estado de RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="e261b-151">Varios códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e261b-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e261b-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e261b-152">Remarks</span></span>

<span data-ttu-id="e261b-153">El miembro **wszGuid** de la estructura de [**\_ entrada Intf**](intf-entry.md) al que apunta el parámetro *pIntf* debe contener un GUID de interfaz para una interfaz LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e261b-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="e261b-154">Se puede recuperar una lista de interfaces de LAN inalámbrica mediante una llamada a la función [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="e261b-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="e261b-155">El archivo de encabezado *wzcsapi. h* y el archivo de biblioteca de importación *wzcsapi. lib* no están disponibles en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e261b-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e261b-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e261b-156">Requirements</span></span>



| <span data-ttu-id="e261b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="e261b-157">Requirement</span></span> | <span data-ttu-id="e261b-158">Value</span><span class="sxs-lookup"><span data-stu-id="e261b-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e261b-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e261b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e261b-160">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e261b-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e261b-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e261b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e261b-162">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e261b-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e261b-163">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e261b-163">End of client support</span></span><br/>    | <span data-ttu-id="e261b-164">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="e261b-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="e261b-165">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e261b-165">End of server support</span></span><br/>    | <span data-ttu-id="e261b-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e261b-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e261b-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e261b-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="e261b-168"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e261b-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e261b-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="e261b-170"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e261b-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e261b-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e261b-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e261b-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e261b-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="e261b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e261b-174">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="e261b-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="e261b-175">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="e261b-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="e261b-176">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e261b-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="e261b-177">**\_entrada Intf**</span><span class="sxs-lookup"><span data-stu-id="e261b-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




