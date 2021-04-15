---
title: WM_BACKUP_RESTORE_STATUS estructura (wmdrmsdk. h)
description: La estructura de estado de restauración de copia de seguridad de WM \_ \_ \_ contiene información sobre una operación de restauración o copia de seguridad de licencias pendiente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709074"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="16786-105">\_Estructura de \_ Estado de restauración de copia de seguridad de WM \_</span><span class="sxs-lookup"><span data-stu-id="16786-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="16786-106">La estructura de **Estado de restauración de copia de seguridad de WM \_ \_ \_** contiene información sobre una operación de restauración o copia de seguridad de licencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="16786-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="16786-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16786-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="16786-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="16786-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="16786-109">**eStatus**</span><span class="sxs-lookup"><span data-stu-id="16786-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="16786-110">Miembro de la enumeración de [**\_ Estado MSDRM**](msdrm-status.md) que especifica el estado.</span><span class="sxs-lookup"><span data-stu-id="16786-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="16786-111">**bstrError**</span><span class="sxs-lookup"><span data-stu-id="16786-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="16786-112">Cadena que contiene el error.</span><span class="sxs-lookup"><span data-stu-id="16786-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16786-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16786-113">Remarks</span></span>

<span data-ttu-id="16786-114">Esta estructura se recibe cuando se llama al método [**IWMDRMLicenseBackupRestoreStatus:: getStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="16786-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="16786-115">Contiene el estado de la operación de copia de seguridad o restauración pendiente en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="16786-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="16786-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16786-116">Requirements</span></span>



| <span data-ttu-id="16786-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16786-117">Requirement</span></span> | <span data-ttu-id="16786-118">Value</span><span class="sxs-lookup"><span data-stu-id="16786-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16786-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16786-119">Header</span></span><br/> | <dl> <span data-ttu-id="16786-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="16786-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16786-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="16786-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16786-122">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="16786-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





