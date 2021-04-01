---
description: Se usa con el \_ IOCTL del minipuerto SCSI de ioctl \_ y el código de control del extremo de la sesión de CTLCODE \_ ISCSITGT de un solo \_ \_ \_ controlador de sesión (0x101) para detener una sesión.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Estructura de ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "103914290"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="37624-103">\_Estructura de \_ detención de sesión de ISCSITGT \_</span><span class="sxs-lookup"><span data-stu-id="37624-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="37624-104">\[La siguiente estructura está disponible para su uso en Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="37624-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="37624-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="37624-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="37624-106">Se usa con el IOCTL del [**\_ \_ minipuerto SCSI de ioctl**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) y el código de control del extremo de la sesión de CTLCODE \_ ISCSITGT de un solo \_ \_ \_ controlador de sesión (0x101) para detener una sesión.</span><span class="sxs-lookup"><span data-stu-id="37624-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="37624-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37624-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="37624-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="37624-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37624-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="37624-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="37624-110">Encabezado obligatorio.</span><span class="sxs-lookup"><span data-stu-id="37624-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="37624-111">**ITNexusHandle**</span><span class="sxs-lookup"><span data-stu-id="37624-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="37624-112">Un identificador opaco que representa una sesión.</span><span class="sxs-lookup"><span data-stu-id="37624-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37624-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37624-113">Requirements</span></span>



| <span data-ttu-id="37624-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37624-114">Requirement</span></span> | <span data-ttu-id="37624-115">Value</span><span class="sxs-lookup"><span data-stu-id="37624-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="37624-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37624-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37624-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="37624-117">None supported</span></span><br/>                               |
| <span data-ttu-id="37624-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37624-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37624-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="37624-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="37624-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="37624-120">End of client support</span></span><br/>    | <span data-ttu-id="37624-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="37624-121">None supported</span></span><br/>                               |
| <span data-ttu-id="37624-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="37624-122">End of server support</span></span><br/>    | <span data-ttu-id="37624-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37624-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="37624-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="37624-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37624-125">Paso a través de destino iSCSI</span><span class="sxs-lookup"><span data-stu-id="37624-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="37624-126">**\_control de e/s SRB \_**</span><span class="sxs-lookup"><span data-stu-id="37624-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
