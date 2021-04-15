---
description: Representa un par clave-valor.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Msvm_KvpExchangeDataItem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688570"
---
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="e1131-103">MSVM \_ KvpExchangeDataItem (clase)</span><span class="sxs-lookup"><span data-stu-id="e1131-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="e1131-104">Representa un par clave-valor.</span><span class="sxs-lookup"><span data-stu-id="e1131-104">Represents a key/value pair.</span></span>

<span data-ttu-id="e1131-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e1131-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1131-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1131-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="e1131-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1131-107">Members</span></span>

<span data-ttu-id="e1131-108">La clase **MSVM \_ KvpExchangeDataItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e1131-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="e1131-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1131-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1131-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1131-110">Properties</span></span>

<span data-ttu-id="e1131-111">La clase **MSVM \_ KvpExchangeDataItem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e1131-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1131-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e1131-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1131-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e1131-115">A short description of the object.</span></span> <span data-ttu-id="e1131-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1131-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1131-117">**Data**</span><span class="sxs-lookup"><span data-stu-id="e1131-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1131-120">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="e1131-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e1131-121">Parte del valor del par clave-valor.</span><span class="sxs-lookup"><span data-stu-id="e1131-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="e1131-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e1131-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1131-125">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e1131-125">A description of the object.</span></span> <span data-ttu-id="e1131-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1131-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1131-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e1131-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1131-130">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e1131-130">A display name for the object.</span></span> <span data-ttu-id="e1131-131">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1131-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1131-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1131-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1131-135">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e1131-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e1131-136">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e1131-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e1131-137">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1131-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1131-138">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e1131-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1131-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1131-141">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="e1131-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e1131-142">Parte de la clave del par clave-valor.</span><span class="sxs-lookup"><span data-stu-id="e1131-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="e1131-143">Clave</span><span class="sxs-lookup"><span data-stu-id="e1131-143">Key</span></span>                                                                                                     | <span data-ttu-id="e1131-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1131-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1131-145"><dt>"CSDVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="e1131-146">Cadena que representa la Service Pack más reciente instalada en el sistema invitado.</span><span class="sxs-lookup"><span data-stu-id="e1131-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="e1131-147">Por ejemplo, "Service Pack 2".</span><span class="sxs-lookup"><span data-stu-id="e1131-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="e1131-148">Si no se ha instalado ningún Service Pack, esta cadena está vacía.</span><span class="sxs-lookup"><span data-stu-id="e1131-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="e1131-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="e1131-150">Cadena que representa el nombre DNS completo que identifica de forma única el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e1131-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="e1131-151">Este nombre es una combinación del nombre de host DNS y el nombre de dominio DNS, con el formato *hostname*. *NombreDeDominio*.</span><span class="sxs-lookup"><span data-stu-id="e1131-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="e1131-152">Si el equipo local es un nodo de un clúster, este valor es el nombre DNS completo del servidor virtual de clústeres.</span><span class="sxs-lookup"><span data-stu-id="e1131-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="e1131-153">Este valor coincide con el nombre devuelto por la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) cuando el parámetro *NameType* es "ComputerNameDnsFullyQualified".</span><span class="sxs-lookup"><span data-stu-id="e1131-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="e1131-154"><dt>"IntegrationServicesVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="e1131-155">Una cadena que representa la versión del Integration Services instalado actualmente en la máquina virtual invitada (por ejemplo, "6.1.7000.0").</span><span class="sxs-lookup"><span data-stu-id="e1131-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="e1131-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="e1131-157">Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv4 asignadas actualmente a la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="e1131-158">La lista se actualiza automáticamente cuando se produce un cambio de configuración de TCP/IP en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="e1131-159">Cada dirección se representa en notación punto-decimal.</span><span class="sxs-lookup"><span data-stu-id="e1131-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="e1131-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="e1131-161">Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv6 asignadas actualmente a la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="e1131-162">La lista se actualiza automáticamente cuando se produce un cambio de configuración de TCP/IP en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="e1131-163">Cada dirección se representa en notación hexadecimal con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e1131-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="e1131-164">No se garantiza que las listas IPv4 e IPv6 estén sincronizadas en todo momento.</span><span class="sxs-lookup"><span data-stu-id="e1131-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="e1131-165"><dt>"OSBuildNumber"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="e1131-166">Cadena que representa el número de compilación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="e1131-167"><dt>"OSEditionId"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="e1131-168">Una cadena que representa la edición (SKU) del sistema operativo de la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="e1131-169">Para obtener una lista de los valores posibles, vea la función [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="e1131-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e1131-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="e1131-171">Cadena que representa el nombre del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="e1131-172">Este valor procede de la siguiente entrada del registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="e1131-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="e1131-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="e1131-174">Cadena que representa el número de versión principal del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="e1131-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="e1131-176">Cadena que representa el número de versión secundaria del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="e1131-177"><dt>"OSPlatformId"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="e1131-178">Cadena que representa la plataforma del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="e1131-179">Los valores posibles de la propiedad **Data** son "1" para indicar un sistema de Windows no compatible y "2" para indicar un sistema de Windows compatible.</span><span class="sxs-lookup"><span data-stu-id="e1131-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="e1131-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="e1131-181">Cadena que representa la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-181">A string that represents the operating system version.</span></span> <span data-ttu-id="e1131-182">El formato de esta cadena es *MajorVersion*. *MinorVersion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="e1131-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="e1131-183">Por ejemplo, "5.2.3790" para Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1131-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e1131-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="e1131-185">Cadena que representa la arquitectura del procesador del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1131-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="e1131-186">Para obtener una lista de valores, vea el miembro **wProcessorArchitecture** de la estructura de [**\_ información del sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="e1131-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="e1131-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="e1131-188">Cadena que representa el tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="e1131-188">A string that represents the product type.</span></span> <span data-ttu-id="e1131-189">Para obtener una lista de valores, vea el miembro **wProductType** de la estructura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="e1131-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="e1131-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="e1131-191">Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv4 en las que la pila RDP de la máquina virtual invitada está escuchando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e1131-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="e1131-192">Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía.</span><span class="sxs-lookup"><span data-stu-id="e1131-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="e1131-193">La lista se actualiza automáticamente siempre que un cambio de configuración de TCP/IP afecte a la pila de RDP en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="e1131-194">Cada dirección se representa en notación punto-decimal.</span><span class="sxs-lookup"><span data-stu-id="e1131-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="e1131-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="e1131-196">Una cadena que contiene una lista delimitada por signos de punto y coma de las direcciones IPv6 en las que la pila RDP de la máquina virtual invitada está escuchando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e1131-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="e1131-197">Si la pila RDP no se está ejecutando actualmente, la cadena estará vacía.</span><span class="sxs-lookup"><span data-stu-id="e1131-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="e1131-198">La lista se actualiza automáticamente siempre que un cambio de configuración de TCP/IP afecte a la pila de RDP en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="e1131-199">Cada dirección se representa en notación hexadecimal con dos puntos.</span><span class="sxs-lookup"><span data-stu-id="e1131-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="e1131-200"><dt>"ServicePackMajor"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="e1131-201">Cadena que representa el número de versión principal de la Service Pack más reciente instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e1131-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="e1131-202"><dt>"ServicePackMinor"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="e1131-203">Cadena que representa el número de versión secundaria de la Service Pack más reciente instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e1131-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="e1131-204"><dt>"SuiteMask"</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="e1131-205">Cadena que representa los conjuntos de productos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e1131-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="e1131-206">Esta cadena es una combinación de cualquiera de los valores del miembro **wSuiteMask** de la estructura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="e1131-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="e1131-207">**Origen**</span><span class="sxs-lookup"><span data-stu-id="e1131-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1131-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1131-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1131-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1131-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1131-210">Origen de los datos.</span><span class="sxs-lookup"><span data-stu-id="e1131-210">The source of the data.</span></span>



| <span data-ttu-id="e1131-211">Value</span><span class="sxs-lookup"><span data-stu-id="e1131-211">Value</span></span>                                                                        | <span data-ttu-id="e1131-212">Significado</span><span class="sxs-lookup"><span data-stu-id="e1131-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1131-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e1131-214">"HostExchangeItems" cuando lo inserte el host.</span><span class="sxs-lookup"><span data-stu-id="e1131-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="e1131-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e1131-216">"GuestExchangeItems" cuando lo inserte la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="e1131-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e1131-218">"GuestIntrinsicExchangeItems" cuando lo rellena automáticamente la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="e1131-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="e1131-220">Indica que el elemento es solo de host y no se comparte con la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="e1131-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="e1131-221">Se usa con la propiedad **HostOnlyItems** de la clase [**\_ KvpExchangeComponentSettingData de MSVM**](msvm-kvpexchangecomponentsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e1131-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1131-222">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1131-222">Remarks</span></span>

<span data-ttu-id="e1131-223">El acceso a la clase **MSVM \_ KvpExchangeDataItem** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e1131-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e1131-224">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e1131-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1131-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1131-225">Requirements</span></span>



| <span data-ttu-id="e1131-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1131-226">Requirement</span></span> | <span data-ttu-id="e1131-227">Value</span><span class="sxs-lookup"><span data-stu-id="e1131-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1131-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1131-228">Minimum supported client</span></span><br/> | <span data-ttu-id="e1131-229">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e1131-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e1131-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1131-230">Minimum supported server</span></span><br/> | <span data-ttu-id="e1131-231">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1131-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1131-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1131-232">Namespace</span></span><br/>                | <span data-ttu-id="e1131-233">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e1131-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e1131-234">MOF</span><span class="sxs-lookup"><span data-stu-id="e1131-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1131-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1131-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1131-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1131-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1131-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1131-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1131-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1131-239">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e1131-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="e1131-240">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e1131-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

