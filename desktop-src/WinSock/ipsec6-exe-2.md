---
description: La configuración de directivas IPSec y asociaciones de seguridad para IPv6 se realiza con Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715122"
---
# <a name="ipsec6exe"></a><span data-ttu-id="d92ea-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="d92ea-103">Ipsec6.exe</span></span>

<span data-ttu-id="d92ea-104">La configuración de directivas IPSec y asociaciones de seguridad para IPv6 se realiza con Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="d92ea-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="d92ea-105">A continuación se muestran los subcomandos Ipsec6.exe:</span><span class="sxs-lookup"><span data-stu-id="d92ea-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="d92ea-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>de **IPSEC6 \[ SP** _Interfaz_ de *_\]_*</span><span class="sxs-lookup"><span data-stu-id="d92ea-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-107">Muestra las directivas de seguridad activas.</span><span class="sxs-lookup"><span data-stu-id="d92ea-107">Displays active security policies.</span></span> <span data-ttu-id="d92ea-108">Como alternativa, se muestran las directivas de seguridad activas para una interfaz específica.</span><span class="sxs-lookup"><span data-stu-id="d92ea-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="d92ea-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**IPSEC6 SA**</span><span class="sxs-lookup"><span data-stu-id="d92ea-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-110">Muestra las asociaciones de seguridad activas.</span><span class="sxs-lookup"><span data-stu-id="d92ea-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="d92ea-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 c \[** _Nombre de archivo (sin extensión)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d92ea-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-112">Crea archivos que se usan para configurar la Directiva de seguridad y las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d92ea-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="d92ea-113">Crea *filename*. SPD para las directivas de seguridad y *filename*. Sad para las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d92ea-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="d92ea-114">Use los archivos creados como plantillas para configurar las directivas de seguridad o las asociaciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d92ea-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="d92ea-115">Los archivos se pueden modificar con un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="d92ea-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="d92ea-116">Para invocar la configuración contenida en los archivos SPD y SAD, use el comando **IPSEC6 a** .</span><span class="sxs-lookup"><span data-stu-id="d92ea-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="d92ea-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 a \[** _Nombre de archivo (sin extensión)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d92ea-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-118">Agrega directivas de seguridad en *filename*. SPD y asociaciones de seguridad en *filename*. Sad a la lista de directivas de seguridad y asociaciones de seguridad activas.</span><span class="sxs-lookup"><span data-stu-id="d92ea-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="d92ea-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 i \[** Nombre de archivo de _Directiva_ *_\] \[_* _(sin extensión)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d92ea-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-120">Agrega directivas de seguridad en *filename*. SPD y asociaciones de seguridad en *filename*. Sad a la lista de directivas de seguridad activas y asociaciones de seguridad a las que hace referencia el número de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="d92ea-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="d92ea-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**IPSEC6 d \[ Type = SP SA \] \[** _IndexNumber_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="d92ea-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="d92ea-122">Elimina las directivas de seguridad o las asociaciones de seguridad de la lista de directivas de seguridad activas y asociaciones de seguridad, según el número de índice (que se muestra con **IPSEC6 SP** o **IPSEC6 SA**).</span><span class="sxs-lookup"><span data-stu-id="d92ea-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



