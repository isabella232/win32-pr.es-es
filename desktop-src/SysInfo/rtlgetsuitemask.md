---
description: Recupera una máscara de bits que identifica los conjuntos de productos disponibles en el sistema. Si se llama a esta función en una aplicación que se ejecuta en el contexto de un silo de servidores, se recupera en su lugar la máscara del conjunto del silo del servidor.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Función RtlGetSuiteMask (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667971"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="c6ae3-104">RtlGetSuiteMask función)</span><span class="sxs-lookup"><span data-stu-id="c6ae3-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="c6ae3-105">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6ae3-106">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c6ae3-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6ae3-107">Recupera una máscara de bits que identifica los conjuntos de productos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="c6ae3-108">Si se llama a esta función en una aplicación que se ejecuta en el contexto de un silo de servidores, se recupera en su lugar la máscara del conjunto del silo del servidor.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ae3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6ae3-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="c6ae3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6ae3-110">Parameters</span></span>

<span data-ttu-id="c6ae3-111">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6ae3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6ae3-112">Return value</span></span>

<span data-ttu-id="c6ae3-113">Máscara de bits que identifica los conjuntos de productos disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="c6ae3-114">La máscara de bits puede incluir los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="c6ae3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6ae3-115">Return value</span></span>                                                                          | <span data-ttu-id="c6ae3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ae3-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6ae3-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c6ae3-118">Microsoft Small Business Server se ha instalado en el sistema, pero es posible que se haya actualizado a otra versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="c6ae3-119">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c6ae3-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="c6ae3-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="c6ae3-122">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="c6ae3-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="c6ae3-124">Los componentes de Microsoft BackOffice están instalados.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="c6ae3-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="c6ae3-126">Se instalan Communications Server 2003, Communications Server 2005, Communications Server 2007 o Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c6ae3-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="c6ae3-128">Terminal Services está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-128">Terminal Services is installed.</span></span> <span data-ttu-id="c6ae3-129">Siempre se establece este valor.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-129">This value is always set.</span></span><br/> <span data-ttu-id="c6ae3-130">Si se establece **TerminalServer** pero no se establece **SingleUserTS** , el sistema se ejecuta en modo de servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c6ae3-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="c6ae3-132">Microsoft Small Business Server se instala con la licencia de cliente restrictiva en vigor.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="c6ae3-133">Consulte la sección Comentarios para obtener más información acerca de esta marca de bits.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="c6ae3-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="c6ae3-135">Windows XP Embedded está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="c6ae3-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="c6ae3-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server están instalados.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="c6ae3-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="c6ae3-139">Escritorio remoto es compatible, pero solo se admite una sesión interactiva.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="c6ae3-140">Este valor se establece a menos que el sistema se ejecute en modo de servidor de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="c6ae3-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="c6ae3-142">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="c6ae3-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="c6ae3-144">Windows Server 2003, Web Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="c6ae3-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="c6ae3-146">Windows Storage Server 2003 R2 o Windows Storage Server 2003 está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="c6ae3-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="c6ae3-148">Windows Server 2003, Compute Cluster Edition está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="c6ae3-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="c6ae3-150">Windows Home Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c6ae3-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6ae3-151">Remarks</span></span>

<span data-ttu-id="c6ae3-152">No debe confiar solo en la marca 0x00000001 para determinar si se ha instalado Small Business Server en el sistema, ya que esta marca y la marca 0x00000020 se establecen cuando se instala este conjunto de productos.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="c6ae3-153">Si actualiza esta instalación a Windows Server, Standard Edition, la marca 0x00000020 se borrará, sin embargo, la marca 0x00000001 permanecerá establecida.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="c6ae3-154">En este caso, indica que se ha instalado Small Business Server en este sistema.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="c6ae3-155">Si esta instalación se actualiza aún más a Windows Server, Enterprise Edition, la marca 0x00000001 permanecerá establecida.</span><span class="sxs-lookup"><span data-stu-id="c6ae3-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ae3-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ae3-156">Requirements</span></span>



| <span data-ttu-id="c6ae3-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ae3-157">Requirement</span></span> | <span data-ttu-id="c6ae3-158">Value</span><span class="sxs-lookup"><span data-stu-id="c6ae3-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ae3-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6ae3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ae3-160">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6ae3-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c6ae3-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6ae3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ae3-162">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6ae3-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c6ae3-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6ae3-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ae3-164"><dt>Ntddk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6ae3-165">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6ae3-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6ae3-166"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6ae3-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6ae3-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ae3-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ae3-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




