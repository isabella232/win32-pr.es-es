---
title: Configuración del compresor y descompresor
description: Configuración del compresor y descompresor
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Administrador de compresión de vídeo (VCM), configurar compresores
- VCM (Administrador de compresión de vídeo), configurar compresores
- Mensaje ICM_CONFIGURE
- ICQueryConfigure (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994154"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="8963c-107">Configuración del compresor y descompresor</span><span class="sxs-lookup"><span data-stu-id="8963c-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="8963c-108">La aplicación puede configurar el compresor o descompresor automáticamente, o puede permitir que el usuario los configure.</span><span class="sxs-lookup"><span data-stu-id="8963c-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="8963c-109">Si es práctico, permita que el usuario configure el compresor o descompresor; Esto le libera de tener en cuenta todas las opciones del compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="8963c-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="8963c-110">El usuario puede configurar el compresor o descompresor mediante un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="8963c-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="8963c-111">Puede enviar el mensaje [**de \_ configuración de ICM**](icm-configure.md) a VCM (o utilizar la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) ) para determinar si un compresor o descompresor puede mostrar un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="8963c-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="8963c-112">Si es así, envíe el \_ mensaje de configuración de ICM (o use la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) ) para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="8963c-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="8963c-113">La aplicación puede enviar los [**mensajes \_ ICM GETSTATE**](icm-getstate.md) y [**ICM \_ SETSTATE**](icm-setstate.md) (o usar las macros [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)y [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) ) para obtener y establecer el estado de un compresor o descompresor.</span><span class="sxs-lookup"><span data-stu-id="8963c-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="8963c-114">Si la aplicación crea o modifica el estado, debe obtener el diseño de los datos del compresor o descompresor antes de restaurar su estado.</span><span class="sxs-lookup"><span data-stu-id="8963c-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="8963c-115">O bien, si la aplicación obtiene el estado de un compresor o descompresor y lo usa para restaurar el estado en una sesión posterior, debe asegurarse de que solo se restaura la información de estado obtenida del compresor o descompresor que está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="8963c-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




