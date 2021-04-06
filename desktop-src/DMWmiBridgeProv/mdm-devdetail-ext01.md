---
title: MDM_DevDetail_Ext01 (clase)
description: La \_ clase Ext01 de DevDetail de MDM \_ controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.
ms.assetid: 8b8cb8e8-a299-4a87-8206-a846a79dd647
keywords:
- MDM_DevDetail_Ext01 (clase)
- MDM_DevDetail_Ext01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DevDetail_Ext01
- MDM_DevDetail_Ext01.InstanceID
- MDM_DevDetail_Ext01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed7d7b68ab192a50a4c029bf573f5de730b8e30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803127"
---
# <a name="mdm_devdetail_ext01-class"></a><span data-ttu-id="610d4-105">\_Clase Ext01 DevDetail de MDM \_</span><span class="sxs-lookup"><span data-stu-id="610d4-105">MDM\_DevDetail\_Ext01 class</span></span>

<span data-ttu-id="610d4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="610d4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="610d4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="610d4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="610d4-108">La **clase \_ \_ Ext01 de DevDetail de MDM** controla el objeto de administración que proporciona parámetros específicos del dispositivo al servidor OMA DM.</span><span class="sxs-lookup"><span data-stu-id="610d4-108">The **MDM\_DevDetail\_Ext01** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="610d4-109">Estos parámetros de dispositivo no se envían automáticamente desde el cliente al servidor, sino que se pueden consultar mediante los comandos OMA DM.</span><span class="sxs-lookup"><span data-stu-id="610d4-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="610d4-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="610d4-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="610d4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="610d4-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Ext01
{
  string InstanceID;
  string ParentID;
  string DeviceHardwareData;
  string WLANMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="610d4-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="610d4-112">Members</span></span>

<span data-ttu-id="610d4-113">La **clase \_ \_ Ext01 de MDM DevDetail** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="610d4-113">The **MDM\_DevDetail\_Ext01** class has these types of members:</span></span>

-   [<span data-ttu-id="610d4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="610d4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="610d4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="610d4-115">Properties</span></span>

<span data-ttu-id="610d4-116">La **clase \_ \_ Ext01 de MDM DevDetail** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="610d4-116">The **MDM\_DevDetail\_Ext01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="610d4-117">DeviceHardwareData</span><span class="sxs-lookup"><span data-stu-id="610d4-117">DeviceHardwareData</span></span>](/windows/client-management/mdm/devdetail-csp#devicehardwaredata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="610d4-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="610d4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="610d4-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="610d4-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="610d4-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="610d4-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="610d4-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="610d4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="610d4-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="610d4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="610d4-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="610d4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="610d4-124">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="610d4-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="610d4-125">Para esta clase, la cadena es "EXT"</span><span class="sxs-lookup"><span data-stu-id="610d4-125">For this class, the string is "Ext"</span></span>

</dd> <dt>

<span data-ttu-id="610d4-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="610d4-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="610d4-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="610d4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="610d4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="610d4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="610d4-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="610d4-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="610d4-130">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="610d4-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="610d4-131">Para esta clase, la cadena es "./DevDetail/".</span><span class="sxs-lookup"><span data-stu-id="610d4-131">For this class, the string is "./DevDetail/"</span></span>

</dd> <dt>

[<span data-ttu-id="610d4-132">WLANMACAddress</span><span class="sxs-lookup"><span data-stu-id="610d4-132">WLANMACAddress</span></span>](/windows/client-management/mdm/devdetail-csp#ext-wlanmacaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="610d4-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="610d4-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="610d4-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="610d4-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="610d4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="610d4-135">Requirements</span></span>



| <span data-ttu-id="610d4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="610d4-136">Requirement</span></span> | <span data-ttu-id="610d4-137">Value</span><span class="sxs-lookup"><span data-stu-id="610d4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610d4-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="610d4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="610d4-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="610d4-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="610d4-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="610d4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="610d4-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="610d4-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="610d4-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="610d4-142">Namespace</span></span><br/>                | <span data-ttu-id="610d4-143">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="610d4-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="610d4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="610d4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="610d4-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="610d4-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="610d4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="610d4-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="610d4-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610d4-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="610d4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610d4-149">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="610d4-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

