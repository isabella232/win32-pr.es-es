---
title: Métodos de la propiedad IADsService (iAds. h)
description: Lea y escriba las propiedades descritas en este tema.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsService ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656529"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="d4c7b-104">Métodos de propiedad IADsService</span><span class="sxs-lookup"><span data-stu-id="d4c7b-104">IADsService Property Methods</span></span>

<span data-ttu-id="d4c7b-105">Los métodos de propiedad de la interfaz [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) leen y escriben las propiedades descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="d4c7b-106">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d4c7b-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d4c7b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4c7b-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d4c7b-108">**Dependencias**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-108">**Dependencies**</span></span>
<span data-ttu-id="d4c7b-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-110">Matriz de nombres **BSTR** de servicios o grupos de carga que se deben cargar para que este servicio pueda cargarse.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="d4c7b-111">La sintaxis de la entrada es "Service:" seguida del nombre del servicio o "Group:" seguido del nombre del grupo de carga.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="d4c7b-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-113">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-114">**DisplayName**</span></span>
<span data-ttu-id="d4c7b-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-116">Nombre descriptivo del servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="d4c7b-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-119">**ErrorControl**</span></span>
<span data-ttu-id="d4c7b-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-121">Acción que se va a realizar si se produce un error en el inicio de este servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="d4c7b-122">Los valores siguientes son válidos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="d4c7b-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ERROR del servicio ADS- \_ \_ \_ omitir \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-124">El programa de inicio registra el error, pero continúa con la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="d4c7b-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_error del servicio ADS \_ \_ normal \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-126">El programa de inicio registra el error y presenta un cuadro de mensaje, pero continúa con la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="d4c7b-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_error grave del servicio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-128">El programa de inicio registra el error.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-128">The startup program logs the error.</span></span> <span data-ttu-id="d4c7b-129">Si se inicia la última configuración válida conocida, la operación de inicio continúa.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="d4c7b-130">De lo contrario, el sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="d4c7b-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_error del servicio ADS \_ \_ crítico \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-132">Si es posible, el programa de inicio registra el error.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="d4c7b-133">Si se está iniciando la última configuración válida conocida, se produce un error en la operación de inicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="d4c7b-134">De lo contrario, el sistema se reinicia con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="d4c7b-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-136">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-137">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-137">**HostComputer**</span></span>
<span data-ttu-id="d4c7b-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-139">Cadena ADsPath del host de este servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="d4c7b-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-141">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="d4c7b-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-144">Nombre del grupo de orden de carga al que pertenece este servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="d4c7b-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-146">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-147">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-147">**Path**</span></span>
<span data-ttu-id="d4c7b-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-149">Ruta de acceso y nombre de archivo del archivo ejecutable de este servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="d4c7b-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-151">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-152">**ServiceAccountName**</span></span>
<span data-ttu-id="d4c7b-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-154">Nombre de la cuenta que usa este servicio para autenticarse en el inicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="d4c7b-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-156">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-157">**ServiceAccountPath**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="d4c7b-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-159">Ruta de acceso de la cuenta especificada por la propiedad **ServiceAccountPath** .</span><span class="sxs-lookup"><span data-stu-id="d4c7b-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="d4c7b-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-161">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-162">**ServiceType**</span></span>
<span data-ttu-id="d4c7b-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-164">La descripción de cómo se presenta un servicio en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="d4c7b-165">Esta propiedad puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="d4c7b-166">\_Controlador de kernel del servicio ADS \* \* \* \* \_ \_ (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="d4c7b-167">\_ \_ Controlador del sistema de archivos del servicio ADS \* \* \* \* \_ \_ (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="d4c7b-168">\_ \_ Proceso propio del servicio ADS \_ \* \* \* \* (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="d4c7b-169">Proceso de recurso compartido de servicio de ADS \* \* \* \* \_ \_ \_ (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d4c7b-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="d4c7b-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-171">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-172">**StartType**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-172">**StartType**</span></span>
<span data-ttu-id="d4c7b-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-174">Determina cómo iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-174">Determines how to start the service.</span></span> <span data-ttu-id="d4c7b-175">Los valores siguientes son válidos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="d4c7b-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_Inicio de arranque del servicio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-177">El servicio es un controlador de dispositivo Iniciado por el cargador del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="d4c7b-178">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="d4c7b-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_ \_ Inicio del sistema de servicio ADS \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-180">El servicio es un controlador de dispositivo Iniciado por la función **IoInitSystem** .</span><span class="sxs-lookup"><span data-stu-id="d4c7b-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="d4c7b-181">Este valor solamente es válido para servicios de controladores.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="d4c7b-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_Inicio automático del servicio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-183">El administrador de control de servicios iniciará automáticamente el servicio durante el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="d4c7b-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>Inicio de la \_ demanda del servicio ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-185">El administrador de control de servicios iniciará el servicio cuando un proceso llame a la función [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="d4c7b-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="d4c7b-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_servicio ADS \_ deshabilitado \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="d4c7b-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="d4c7b-187">No se puede iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-187">The service cannot be started.</span></span> <span data-ttu-id="d4c7b-188">Intenta iniciar el resultado del servicio en el servicio de error de código de error **\_ \_ deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="d4c7b-189">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-190">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-191">**StartupParameters**</span></span>
<span data-ttu-id="d4c7b-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-193">Parámetros pasados al servicio en el inicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="d4c7b-194">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-195">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d4c7b-196">**Versión**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-196">**Version**</span></span>
<span data-ttu-id="d4c7b-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d4c7b-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="d4c7b-198">Versión del servicio.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="d4c7b-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4c7b-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d4c7b-200">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d4c7b-201">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d4c7b-201">Examples</span></span>

<span data-ttu-id="d4c7b-202">En el ejemplo de código siguiente se muestra cómo enumerar todos los servicios del sistema disponibles que se ejecutan en el equipo host, "MiEquipo", junto con la ubicación para buscar los ejecutables de los servicios.</span><span class="sxs-lookup"><span data-stu-id="d4c7b-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="d4c7b-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4c7b-203">Requirements</span></span>



| <span data-ttu-id="d4c7b-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4c7b-204">Requirement</span></span> | <span data-ttu-id="d4c7b-205">Value</span><span class="sxs-lookup"><span data-stu-id="d4c7b-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c7b-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4c7b-206">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c7b-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4c7b-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4c7b-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4c7b-208">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c7b-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4c7b-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4c7b-210">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4c7b-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4c7b-211"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4c7b-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d4c7b-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4c7b-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4c7b-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c7b-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d4c7b-214">IID</span><span class="sxs-lookup"><span data-stu-id="d4c7b-214">IID</span></span><br/>                      | <span data-ttu-id="d4c7b-215">IID \_ IADsService se define como 68AF66E0-31CA-11cf-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="d4c7b-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d4c7b-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4c7b-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c7b-217">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="d4c7b-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="d4c7b-218">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="d4c7b-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

