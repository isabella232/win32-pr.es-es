---
description: Representa una colección que proporciona capacidades informáticas y consta de \_ objetos ManagedSystemElement de CIM.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: CIM_ComputerSystem (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688656"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="67f2e-103">CIM_ComputerSystem (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="67f2e-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="67f2e-104">Representa una colección que proporciona capacidades informáticas y consta de objetos [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2e-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67f2e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="67f2e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="67f2e-106">Members</span></span>

<span data-ttu-id="67f2e-107">La clase de **\_ ComputerSystem de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67f2e-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="67f2e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="67f2e-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="67f2e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67f2e-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67f2e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="67f2e-110">Methods</span></span>

<span data-ttu-id="67f2e-111">La clase de **\_ ComputerSystem de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="67f2e-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="67f2e-112">Método</span><span class="sxs-lookup"><span data-stu-id="67f2e-112">Method</span></span>                                                    | <span data-ttu-id="67f2e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="67f2e-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67f2e-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="67f2e-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="67f2e-115">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="67f2e-115">This method is deprecated.</span></span> <span data-ttu-id="67f2e-116">En su lugar, use el método **RequestPowerStateChange** de la clase **\_ PowerManagementService de CIM** .</span><span class="sxs-lookup"><span data-stu-id="67f2e-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="67f2e-117">**Descripción desusada:** Establece el estado de energía del equipo.</span><span class="sxs-lookup"><span data-stu-id="67f2e-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="67f2e-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67f2e-118">Properties</span></span>

<span data-ttu-id="67f2e-119">La clase de **\_ ComputerSystem de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="67f2e-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67f2e-120">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="67f2e-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f2e-121">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67f2e-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67f2e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-123">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. INCITS-T11 \| Platform \| PlatformType "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**OtherDedicatedDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="67f2e-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="67f2e-124">El propósito y las características del equipo.</span><span class="sxs-lookup"><span data-stu-id="67f2e-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="67f2e-125">Por ejemplo, un sistema dedicado a la impresión podría especificar "11" (imprimir).</span><span class="sxs-lookup"><span data-stu-id="67f2e-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="67f2e-126">Un sistema de uso general con capacidades de impresión se puede establecer en "0" (no dedicado) y "11" (imprimir).</span><span class="sxs-lookup"><span data-stu-id="67f2e-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="67f2e-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**No dedicado** (0)</span><span class="sxs-lookup"><span data-stu-id="67f2e-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67f2e-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="67f2e-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67f2e-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (2)</span><span class="sxs-lookup"><span data-stu-id="67f2e-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="67f2e-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Almacenamiento** (3)</span><span class="sxs-lookup"><span data-stu-id="67f2e-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="67f2e-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Enrutador** (4)</span><span class="sxs-lookup"><span data-stu-id="67f2e-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="67f2e-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Modificador** (5)</span><span class="sxs-lookup"><span data-stu-id="67f2e-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="67f2e-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Conmutador de capa 3** (6)</span><span class="sxs-lookup"><span data-stu-id="67f2e-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="67f2e-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Conmutador de oficina central** (7)</span><span class="sxs-lookup"><span data-stu-id="67f2e-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="67f2e-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span><span class="sxs-lookup"><span data-stu-id="67f2e-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="67f2e-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Servidor de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="67f2e-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="67f2e-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span><span class="sxs-lookup"><span data-stu-id="67f2e-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="67f2e-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Imprimir** (11)</span><span class="sxs-lookup"><span data-stu-id="67f2e-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="67f2e-139"><span id="I_O"></span><span id="i_o"></span>**E/s** (12)</span><span class="sxs-lookup"><span data-stu-id="67f2e-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="67f2e-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Almacenamiento en caché Web** (13)</span><span class="sxs-lookup"><span data-stu-id="67f2e-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="67f2e-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Administración** (14)</span><span class="sxs-lookup"><span data-stu-id="67f2e-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-142">Esta instancia está dedicada a hospedar el software de administración del sistema</span><span class="sxs-lookup"><span data-stu-id="67f2e-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="67f2e-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Bloquear servidor** (15)</span><span class="sxs-lookup"><span data-stu-id="67f2e-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="67f2e-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Servidor de archivos** (16)</span><span class="sxs-lookup"><span data-stu-id="67f2e-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="67f2e-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Dispositivo de usuario móvil** (17)</span><span class="sxs-lookup"><span data-stu-id="67f2e-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-146">Un ejemplo de dispositivo de usuario dedicado es un teléfono móvil o un escáner de código de barras en un almacén que se comunica a través de la frecuencia de radio.</span><span class="sxs-lookup"><span data-stu-id="67f2e-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="67f2e-147">Estos sistemas están bastante limitados en cuanto a funcionalidad y programación, y no se consideran plataformas informáticas de uso general.</span><span class="sxs-lookup"><span data-stu-id="67f2e-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="67f2e-148">Como alternativa, un ejemplo de un sistema móvil que es "uso general" (es decir, no está dedicado) es un equipo que se mantiene a mano.</span><span class="sxs-lookup"><span data-stu-id="67f2e-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="67f2e-149">Aunque está limitado en su programación, el nuevo software se puede descargar y su funcionalidad se expande por el usuario.</span><span class="sxs-lookup"><span data-stu-id="67f2e-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="67f2e-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repetidor** (18)</span><span class="sxs-lookup"><span data-stu-id="67f2e-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="67f2e-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/extender** (19)</span><span class="sxs-lookup"><span data-stu-id="67f2e-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="67f2e-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Puerta de enlace** (20)</span><span class="sxs-lookup"><span data-stu-id="67f2e-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="67f2e-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualizador de almacenamiento** (21)</span><span class="sxs-lookup"><span data-stu-id="67f2e-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="67f2e-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Biblioteca multimedia** (22)</span><span class="sxs-lookup"><span data-stu-id="67f2e-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="67f2e-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span><span class="sxs-lookup"><span data-stu-id="67f2e-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="67f2e-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Director de NAS** (24)</span><span class="sxs-lookup"><span data-stu-id="67f2e-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="67f2e-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**NAS independiente** (25)</span><span class="sxs-lookup"><span data-stu-id="67f2e-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="67f2e-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span><span class="sxs-lookup"><span data-stu-id="67f2e-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="67f2e-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Teléfono IP** (27)</span><span class="sxs-lookup"><span data-stu-id="67f2e-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="67f2e-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Controlador de administración** (28)</span><span class="sxs-lookup"><span data-stu-id="67f2e-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-161">Esta instancia representa el hardware especializado dedicado a la administración de sistemas (es decir, un controlador de administración de placa base (BMC) o un procesador de servicio).</span><span class="sxs-lookup"><span data-stu-id="67f2e-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="67f2e-162">El ámbito de administración de un "controlador de administración" suele ser un único sistema administrado en el que está contenido.</span><span class="sxs-lookup"><span data-stu-id="67f2e-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="67f2e-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Administrador de chasis** (29)</span><span class="sxs-lookup"><span data-stu-id="67f2e-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-164">Esta instancia representa un sistema dedicado a la administración de un chasis de hoja y sus dispositivos contenidos.</span><span class="sxs-lookup"><span data-stu-id="67f2e-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="67f2e-165">Este valor se utiliza para representar un controlador de estantería.</span><span class="sxs-lookup"><span data-stu-id="67f2e-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="67f2e-166">Un "Administrador de chasis" es un punto de agregación para la administración y puede depender de controladores de administración subordinados para la administración de partes constituyentes.</span><span class="sxs-lookup"><span data-stu-id="67f2e-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="67f2e-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Controladora RAID basado en host** (30)</span><span class="sxs-lookup"><span data-stu-id="67f2e-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-168">Esta instancia representa un controlador de almacenamiento RAID incluido en un equipo host.</span><span class="sxs-lookup"><span data-stu-id="67f2e-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="67f2e-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Contenedor de dispositivos de almacenamiento** (31)</span><span class="sxs-lookup"><span data-stu-id="67f2e-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-170">Esta instancia representa un contenedor que contiene dispositivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="67f2e-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="67f2e-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Escritorio** (32)</span><span class="sxs-lookup"><span data-stu-id="67f2e-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="67f2e-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portátil** (33)</span><span class="sxs-lookup"><span data-stu-id="67f2e-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="67f2e-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Biblioteca de cintas virtuales** (34)</span><span class="sxs-lookup"><span data-stu-id="67f2e-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-174">La emulación de una biblioteca de cintas por un sistema de biblioteca virtual.</span><span class="sxs-lookup"><span data-stu-id="67f2e-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="67f2e-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Sistema de biblioteca virtual** (35)</span><span class="sxs-lookup"><span data-stu-id="67f2e-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-176">Usa el almacenamiento en disco para emular las bibliotecas de cintas</span><span class="sxs-lookup"><span data-stu-id="67f2e-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="67f2e-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC de red/cliente ligero** (36)</span><span class="sxs-lookup"><span data-stu-id="67f2e-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="67f2e-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Conmutador FC** (37)</span><span class="sxs-lookup"><span data-stu-id="67f2e-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-179">Dedicado para cambiar fotogramas de canal de fibra de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="67f2e-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="67f2e-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Conmutador Ethernet** (38)</span><span class="sxs-lookup"><span data-stu-id="67f2e-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="67f2e-181">Dedicado para cambiar fotogramas Ethernet de capa 2</span><span class="sxs-lookup"><span data-stu-id="67f2e-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="67f2e-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="67f2e-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="67f2e-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32568.. 65535)</span><span class="sxs-lookup"><span data-stu-id="67f2e-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67f2e-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="67f2e-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f2e-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67f2e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67f2e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-187">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="67f2e-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="67f2e-188">Formato del nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="67f2e-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="67f2e-189">("Otro")</span><span class="sxs-lookup"><span data-stu-id="67f2e-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-190">("IP")</span><span class="sxs-lookup"><span data-stu-id="67f2e-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-191">("Marcar")</span><span class="sxs-lookup"><span data-stu-id="67f2e-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-192">("HID")</span><span class="sxs-lookup"><span data-stu-id="67f2e-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-193">("NWA")</span><span class="sxs-lookup"><span data-stu-id="67f2e-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-194">("HWA")</span><span class="sxs-lookup"><span data-stu-id="67f2e-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-195">("X25")</span><span class="sxs-lookup"><span data-stu-id="67f2e-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-196">("ISDN")</span><span class="sxs-lookup"><span data-stu-id="67f2e-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-197">("IPX")</span><span class="sxs-lookup"><span data-stu-id="67f2e-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-198">("DCC")</span><span class="sxs-lookup"><span data-stu-id="67f2e-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-199">("ICD")</span><span class="sxs-lookup"><span data-stu-id="67f2e-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-200">("E. 164")</span><span class="sxs-lookup"><span data-stu-id="67f2e-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-201">("SNA")</span><span class="sxs-lookup"><span data-stu-id="67f2e-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-202">("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="67f2e-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-203">("WWN")</span><span class="sxs-lookup"><span data-stu-id="67f2e-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="67f2e-204">("NAA")</span><span class="sxs-lookup"><span data-stu-id="67f2e-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67f2e-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="67f2e-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f2e-206">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="67f2e-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67f2e-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-208">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Dedicado**")</span><span class="sxs-lookup"><span data-stu-id="67f2e-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="67f2e-209">Describe cómo o por qué el sistema está dedicado cuando la matriz **dedicada** incluye el valor 2 (otro).</span><span class="sxs-lookup"><span data-stu-id="67f2e-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="67f2e-210">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="67f2e-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f2e-211">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67f2e-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67f2e-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-213">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de alimentación del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="67f2e-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="67f2e-214">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="67f2e-214">This property is deprecated.</span></span> <span data-ttu-id="67f2e-215">En su lugar, use el método **PowerChangeCapabilities** de la clase **\_ PowerManagementCapabilitiesCIM \_ PowerManagementService de CIM** .</span><span class="sxs-lookup"><span data-stu-id="67f2e-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="67f2e-216">**Descripción desusada:** Las capacidades de administración de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="67f2e-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67f2e-217">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="67f2e-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="67f2e-218">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="67f2e-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67f2e-219">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="67f2e-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67f2e-220">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="67f2e-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="67f2e-221">**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="67f2e-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="67f2e-222">**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="67f2e-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="67f2e-223">**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="67f2e-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="67f2e-224">Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="67f2e-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67f2e-225">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="67f2e-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f2e-226">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67f2e-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67f2e-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67f2e-228">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Seguridad de hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="67f2e-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="67f2e-229">Indica si el sistema admite la operación de restablecimiento de hardware.</span><span class="sxs-lookup"><span data-stu-id="67f2e-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67f2e-230">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="67f2e-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67f2e-231">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="67f2e-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67f2e-232">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="67f2e-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67f2e-233">**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="67f2e-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="67f2e-234">**No implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="67f2e-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="67f2e-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67f2e-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="67f2e-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67f2e-236">Requirements</span></span>



| <span data-ttu-id="67f2e-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f2e-237">Requirement</span></span> | <span data-ttu-id="67f2e-238">Value</span><span class="sxs-lookup"><span data-stu-id="67f2e-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f2e-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f2e-239">Minimum supported client</span></span><br/> | <span data-ttu-id="67f2e-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="67f2e-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="67f2e-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f2e-241">Minimum supported server</span></span><br/> | <span data-ttu-id="67f2e-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67f2e-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="67f2e-243">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67f2e-243">Namespace</span></span><br/>                | <span data-ttu-id="67f2e-244">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="67f2e-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67f2e-245">MOF</span><span class="sxs-lookup"><span data-stu-id="67f2e-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67f2e-246"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67f2e-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67f2e-247">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67f2e-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f2e-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67f2e-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67f2e-249">Vea también</span><span class="sxs-lookup"><span data-stu-id="67f2e-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f2e-250">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="67f2e-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

