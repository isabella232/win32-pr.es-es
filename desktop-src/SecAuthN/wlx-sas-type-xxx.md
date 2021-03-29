---
description: Los valores definen un tipo de SAS específico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648555"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="3a7e7-103">WLX \_ SAS \_ tipo \_ XXX</span><span class="sxs-lookup"><span data-stu-id="3a7e7-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="3a7e7-104">\[La \_ constante de \_ tipo \_ XXX de SAS de WLX ya no está disponible para su uso en Windows Server 2008 y Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="3a7e7-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="3a7e7-105">Los valores de **\_ \_ tipo \_ XXX de SAS de WLX** definen un tipo de SAS específico.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="3a7e7-106">Los archivos dll de GINA se omiten en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="3a7e7-107">Todos los valores de cero a 127 se reservan para los tipos definidos por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="3a7e7-108">Los valores por encima de 127 están disponibles para los tipos definidos por el cliente.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="3a7e7-109">Los tipos siguientes se pasan a las funciones que tienen un parámetro *dwSasType* .</span><span class="sxs-lookup"><span data-stu-id="3a7e7-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="3a7e7-110">Constante</span><span class="sxs-lookup"><span data-stu-id="3a7e7-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="3a7e7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a7e7-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="3a7e7-112"><dt>**WLX \_ tipo de SAS \_ \_ Ctrl \_ ALT \_ Supr**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="3a7e7-113">Indica que un usuario ha escrito las SA estándar CTRL + ALT + SUPR.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="3a7e7-114"><dt>**WLX \_ SAS \_ Type \_ SC \_ Insert**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="3a7e7-115">Indica que se ha insertado una [*tarjeta inteligente*](../secgloss/s-gly.md) en un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="3a7e7-116"><dt>**WLX \_ SAS \_ tipo \_ SC \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="3a7e7-117">Indica que se ha quitado una tarjeta inteligente de un dispositivo compatible.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="3a7e7-118"><dt>**WLX \_ tipo de SAS \_ \_ SCRNSVR \_ actividad**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="3a7e7-119">Indica que la actividad del teclado o del mouse se produjo mientras estaba activo un protector de pantalla seguro.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="3a7e7-120"><dt>**WLX \_ tipo de SAS \_ \_ SCRNSVR \_ tiempo de espera**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="3a7e7-121">Indica que se ha producido la activación del protector de pantalla debido a la inactividad del teclado y del mouse.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="3a7e7-122"><dt>**WLX \_ \_ tiempo de espera de tipo SAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="3a7e7-123">Indica que no se ha recibido ninguna entrada de usuario dentro del período de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="3a7e7-124"><dt>**\_cierre de \_ \_ sesión de usuario de tipo SAS de WLX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="3a7e7-125">Indica que el usuario está cerrando la sesión del sistema.</span><span class="sxs-lookup"><span data-stu-id="3a7e7-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="3a7e7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a7e7-126">Requirements</span></span>



| <span data-ttu-id="3a7e7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a7e7-127">Requirement</span></span> | <span data-ttu-id="3a7e7-128">Value</span><span class="sxs-lookup"><span data-stu-id="3a7e7-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7e7-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a7e7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7e7-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3a7e7-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3a7e7-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a7e7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7e7-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a7e7-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3a7e7-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3a7e7-133">End of client support</span></span><br/>    | <span data-ttu-id="3a7e7-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a7e7-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="3a7e7-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3a7e7-135">End of server support</span></span><br/>    | <span data-ttu-id="3a7e7-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3a7e7-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="3a7e7-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a7e7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a7e7-138"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a7e7-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
