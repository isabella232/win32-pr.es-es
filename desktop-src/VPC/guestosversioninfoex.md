---
title: Estructura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contiene información de versión del sistema operativo para el sistema operativo invitado.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- GUESTOSVERSIONINFOEX estructura virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150485"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="a65c8-104">Estructura GUESTOSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="a65c8-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="a65c8-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a65c8-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a65c8-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a65c8-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a65c8-107">Contiene información de versión del sistema operativo para el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65c8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a65c8-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="a65c8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a65c8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a65c8-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="a65c8-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-111">Tamaño de esta estructura de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a65c8-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="a65c8-112">Establezca este miembro en `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="a65c8-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="a65c8-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-114">Número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="a65c8-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="a65c8-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-116">Número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="a65c8-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="a65c8-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-118">Número de compilación.</span><span class="sxs-lookup"><span data-stu-id="a65c8-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="a65c8-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-120">Plataforma del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a65c8-120">The operating system platform.</span></span> <span data-ttu-id="a65c8-121">Este miembro puede ser **la \_ plataforma ver \_ Win32 \_ NT** (2).</span><span class="sxs-lookup"><span data-stu-id="a65c8-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="a65c8-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-123">Una cadena terminada en null, como "Service Pack 3", que indica el último Service Pack instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a65c8-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="a65c8-124">Si no se ha instalado ningún Service Pack, la cadena está vacía.</span><span class="sxs-lookup"><span data-stu-id="a65c8-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="a65c8-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-126">Número de versión principal del Service Pack más reciente instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="a65c8-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-128">El número de versión secundaria del último Service Pack instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="a65c8-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="a65c8-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-130">Máscara de máscara que identifica los conjuntos de productos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a65c8-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="a65c8-131">Este miembro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a65c8-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="a65c8-132">Value</span><span class="sxs-lookup"><span data-stu-id="a65c8-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a65c8-133">Significado</span><span class="sxs-lookup"><span data-stu-id="a65c8-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="a65c8-134"><dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="a65c8-135">Los componentes de Microsoft BackOffice están instalados.</span><span class="sxs-lookup"><span data-stu-id="a65c8-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="a65c8-136"><dt>**Ver \_ PAQUETE \_**</dt> de la hoja <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="a65c8-137">Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="a65c8-138"><dt>**Ver \_ CONJUNTO de \_ \_ servidores de proceso**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="a65c8-139">Windows Server 2003, Compute Cluster Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="a65c8-140"><dt>**Ver \_ CONJUNTO de \_ centros**</dt> de <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="a65c8-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="a65c8-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="a65c8-142"><dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="a65c8-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="a65c8-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="a65c8-144">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="a65c8-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="a65c8-145"><dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="a65c8-146">Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="a65c8-147"><dt>**Ver \_ 0x00000200 \_ personal de Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="a65c8-148">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="a65c8-149"><dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="a65c8-150">Escritorio remoto es compatible, pero solo se admite una sesión interactiva.</span><span class="sxs-lookup"><span data-stu-id="a65c8-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="a65c8-151">Este valor se establece a menos que el sistema se ejecute en modo de servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a65c8-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="a65c8-152"><dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="a65c8-153">Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="a65c8-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="a65c8-154">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="a65c8-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="a65c8-155"><dt>**Ver \_ SUITE de uso \_ \_ restringido de SMALLBUSINESS**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="a65c8-156">Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.</span><span class="sxs-lookup"><span data-stu-id="a65c8-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="a65c8-157">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="a65c8-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="a65c8-158"><dt>**Ver \_ SUITE de \_ Storage \_ Server**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="a65c8-159">Windows Storage Server 2003 R2 o Windows Storage Server 2003 están instalados.</span><span class="sxs-lookup"><span data-stu-id="a65c8-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="a65c8-160"><dt>**Ver \_ CONJUNTO de \_ terminales**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="a65c8-161">Terminal Services está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-161">Terminal Services is installed.</span></span> <span data-ttu-id="a65c8-162">Siempre se establece este valor.</span><span class="sxs-lookup"><span data-stu-id="a65c8-162">This value is always set.</span></span><br/> <span data-ttu-id="a65c8-163">Si se establece el **\_ \_ terminal de versión del paquete** , pero no se establece **Ver \_ Suite \_ SINGLEUSERTS** , el sistema se ejecuta en modo de servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a65c8-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="a65c8-164"><dt>**Ver \_ SUITE \_ qu \_ Server**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="a65c8-165">Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="a65c8-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="a65c8-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="a65c8-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-167">Cualquier información adicional sobre el sistema.</span><span class="sxs-lookup"><span data-stu-id="a65c8-167">Any additional information about the system.</span></span> <span data-ttu-id="a65c8-168">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a65c8-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="a65c8-169">Value</span><span class="sxs-lookup"><span data-stu-id="a65c8-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="a65c8-170">Significado</span><span class="sxs-lookup"><span data-stu-id="a65c8-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="a65c8-171"><dt>**Ver \_ \_ \_ Controlador de dominio NT**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="a65c8-172">El sistema es un controlador de dominio y el sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a65c8-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="a65c8-173"><dt>**Ver \_ 0x0000003 de NT \_ Server**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="a65c8-174">El sistema operativo es Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a65c8-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="a65c8-175">Tenga en cuenta que un servidor que también es un controlador de dominio se indica como controlador de dominio de NT de ver, no como **\_ \_ servidor de NT**. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a65c8-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="a65c8-176"><dt>**Ver \_ NT \_ Workstation**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="a65c8-177">El sistema operativo es Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a65c8-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="a65c8-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="a65c8-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="a65c8-179">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a65c8-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a65c8-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65c8-180">Requirements</span></span>



| <span data-ttu-id="a65c8-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65c8-181">Requirement</span></span> | <span data-ttu-id="a65c8-182">Value</span><span class="sxs-lookup"><span data-stu-id="a65c8-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a65c8-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a65c8-183">Minimum supported client</span></span><br/> | <span data-ttu-id="a65c8-184">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a65c8-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a65c8-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a65c8-185">Minimum supported server</span></span><br/> | <span data-ttu-id="a65c8-186">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a65c8-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a65c8-187">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a65c8-187">End of client support</span></span><br/>    | <span data-ttu-id="a65c8-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a65c8-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a65c8-189">Producto</span><span class="sxs-lookup"><span data-stu-id="a65c8-189">Product</span></span><br/>                  | <span data-ttu-id="a65c8-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a65c8-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a65c8-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a65c8-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65c8-192"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65c8-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a65c8-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="a65c8-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65c8-194">**IVMGuestOS::GetOsVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="a65c8-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

