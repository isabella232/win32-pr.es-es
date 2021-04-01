---
description: La tabla AppId o la tabla del registro especifica que el instalador configura y registra los servidores DCOM para realizar una de las siguientes acciones durante una instalación.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabla AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909109"
---
# <a name="appid-table"></a><span data-ttu-id="aca36-103">Tabla AppId</span><span class="sxs-lookup"><span data-stu-id="aca36-103">AppId Table</span></span>

<span data-ttu-id="aca36-104">La tabla AppId o la [tabla del registro](registry-table.md) especifica que el instalador configura y registra los servidores DCOM para realizar una de las siguientes acciones durante una instalación.</span><span class="sxs-lookup"><span data-stu-id="aca36-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="aca36-105">Ejecute el servidor DCOM con una identidad diferente a la del usuario que activa el servidor.</span><span class="sxs-lookup"><span data-stu-id="aca36-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="aca36-106">Por ejemplo, para configurar un servidor DCOM para que se ejecute siempre como usuario interactivo o como usuario predefinido.</span><span class="sxs-lookup"><span data-stu-id="aca36-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="aca36-107">Ejecute el servidor DCOM como servicio.</span><span class="sxs-lookup"><span data-stu-id="aca36-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="aca36-108">Configure el acceso de seguridad predeterminado para el servidor DCOM.</span><span class="sxs-lookup"><span data-stu-id="aca36-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="aca36-109">Registre el servidor DCOM para que se active en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="aca36-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="aca36-110">Esta tabla se procesa en la instalación del componente asociado al servidor DCOM en la \_ columna componente de la [tabla clase](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="aca36-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="aca36-111">No se anuncia un AppId.</span><span class="sxs-lookup"><span data-stu-id="aca36-111">An AppId is not advertised.</span></span>

<span data-ttu-id="aca36-112">La tabla AppId tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="aca36-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="aca36-113">Columna</span><span class="sxs-lookup"><span data-stu-id="aca36-113">Column</span></span>               | <span data-ttu-id="aca36-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="aca36-114">Type</span></span>                       | <span data-ttu-id="aca36-115">Clave</span><span class="sxs-lookup"><span data-stu-id="aca36-115">Key</span></span> | <span data-ttu-id="aca36-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="aca36-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="aca36-117">AppId</span><span class="sxs-lookup"><span data-stu-id="aca36-117">AppId</span></span>                | [<span data-ttu-id="aca36-118">GUID</span><span class="sxs-lookup"><span data-stu-id="aca36-118">GUID</span></span>](guid.md)           | <span data-ttu-id="aca36-119">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-119">Y</span></span>   | <span data-ttu-id="aca36-120">N</span><span class="sxs-lookup"><span data-stu-id="aca36-120">N</span></span>        |
| <span data-ttu-id="aca36-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="aca36-121">RemoteServerName</span></span>     | [<span data-ttu-id="aca36-122">Formatea</span><span class="sxs-lookup"><span data-stu-id="aca36-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="aca36-123">N</span><span class="sxs-lookup"><span data-stu-id="aca36-123">N</span></span>   | <span data-ttu-id="aca36-124">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-124">Y</span></span>        |
| <span data-ttu-id="aca36-125">LocalService (Servicio local)</span><span class="sxs-lookup"><span data-stu-id="aca36-125">LocalService</span></span>         | [<span data-ttu-id="aca36-126">Texto</span><span class="sxs-lookup"><span data-stu-id="aca36-126">Text</span></span>](text.md)           | <span data-ttu-id="aca36-127">N</span><span class="sxs-lookup"><span data-stu-id="aca36-127">N</span></span>   | <span data-ttu-id="aca36-128">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-128">Y</span></span>        |
| <span data-ttu-id="aca36-129">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="aca36-129">ServiceParameters</span></span>    | [<span data-ttu-id="aca36-130">Texto</span><span class="sxs-lookup"><span data-stu-id="aca36-130">Text</span></span>](text.md)           | <span data-ttu-id="aca36-131">N</span><span class="sxs-lookup"><span data-stu-id="aca36-131">N</span></span>   | <span data-ttu-id="aca36-132">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-132">Y</span></span>        |
| <span data-ttu-id="aca36-133">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="aca36-133">DllSurrogate</span></span>         | [<span data-ttu-id="aca36-134">Texto</span><span class="sxs-lookup"><span data-stu-id="aca36-134">Text</span></span>](text.md)           | <span data-ttu-id="aca36-135">N</span><span class="sxs-lookup"><span data-stu-id="aca36-135">N</span></span>   | <span data-ttu-id="aca36-136">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-136">Y</span></span>        |
| <span data-ttu-id="aca36-137">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="aca36-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="aca36-138">Entero</span><span class="sxs-lookup"><span data-stu-id="aca36-138">Integer</span></span>](integer.md)     | <span data-ttu-id="aca36-139">N</span><span class="sxs-lookup"><span data-stu-id="aca36-139">N</span></span>   | <span data-ttu-id="aca36-140">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-140">Y</span></span>        |
| <span data-ttu-id="aca36-141">RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="aca36-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="aca36-142">Entero</span><span class="sxs-lookup"><span data-stu-id="aca36-142">Integer</span></span>](integer.md)     | <span data-ttu-id="aca36-143">N</span><span class="sxs-lookup"><span data-stu-id="aca36-143">N</span></span>   | <span data-ttu-id="aca36-144">Y</span><span class="sxs-lookup"><span data-stu-id="aca36-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="aca36-145">Columnas</span><span class="sxs-lookup"><span data-stu-id="aca36-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="aca36-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span><span class="sxs-lookup"><span data-stu-id="aca36-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="aca36-147">La columna AppId de la [tabla de clase](class-table.md) es una clave externa de esta columna de la tabla AppID.</span><span class="sxs-lookup"><span data-stu-id="aca36-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="aca36-148">Esta columna contiene el valor AppId que se escribirá en el CLSID y creará la clave AppId GUID en HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="aca36-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="aca36-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="aca36-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="aca36-150">Esta columna contiene el valor "RemoteServerName" = <xxxx> que se escribirá en HKCR \\ AppID \\ {AppID} \\ .</span><span class="sxs-lookup"><span data-stu-id="aca36-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="aca36-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="aca36-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="aca36-152">Esta columna contiene el valor de LocalService que se escribirá en HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="aca36-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="aca36-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="aca36-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="aca36-154">Esta columna contiene el valor de ServiceParameters que se escribirá en HKCR \\ AppID \\ {AppID>} "ServiceParameters".</span><span class="sxs-lookup"><span data-stu-id="aca36-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="aca36-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="aca36-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="aca36-156">Esta columna contiene el valor de DllSurrogate que se escribirá en HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="aca36-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="aca36-157">Si esta columna está presente, normalmente será una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="aca36-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="aca36-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="aca36-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="aca36-159">Un valor entero distinto de cero en este campo hace que Windows Installer escriba HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" en el registro.</span><span class="sxs-lookup"><span data-stu-id="aca36-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="aca36-160">Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aca36-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="aca36-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="aca36-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="aca36-162">Un valor entero distinto de cero en este campo hace que Windows Installer escriba el identificador \\ AppID \\ {AppID>} "runas" = "usuario interactivo" en el registro.</span><span class="sxs-lookup"><span data-stu-id="aca36-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="aca36-163">Si el campo se deja vacío o tiene un valor de cero, no se escribirá ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aca36-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aca36-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aca36-164">Remarks</span></span>

<span data-ttu-id="aca36-165">Esta tabla la usan la [acción RegisterClassInfo](registerclassinfo-action.md) y la [acción UnregisterClassInfo](unregisterclassinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="aca36-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="aca36-166">Tenga en cuenta que la tabla AppId no tiene una columna para registrar un nombre predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aca36-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="aca36-167">Por lo tanto, en los casos en los que tenga que escribir un nombre descriptivo como el valor de nombre predeterminado, debe registrarse mediante la [tabla del registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="aca36-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="aca36-168">Validación</span><span class="sxs-lookup"><span data-stu-id="aca36-168">Validation</span></span>

<dl>

[<span data-ttu-id="aca36-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="aca36-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="aca36-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="aca36-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="aca36-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="aca36-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="aca36-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="aca36-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="aca36-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="aca36-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="aca36-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="aca36-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



