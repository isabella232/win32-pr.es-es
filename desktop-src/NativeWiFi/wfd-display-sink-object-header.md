---
description: Describe los datos del objeto de receptor de pantalla incluidos en un resultado de notificación o notificación.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER estructura (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909426"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="25869-103">\_Estructura de \_ encabezado de objeto de receptor de visualización de \_ WFD \_</span><span class="sxs-lookup"><span data-stu-id="25869-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="25869-104">La estructura de encabezado de objeto del receptor de visualización de WFD describe los datos del objeto de receptor de pantalla incluidos en un resultado de notificación o notificación. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25869-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="25869-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25869-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="25869-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="25869-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="25869-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="25869-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="25869-108">Tipo del objeto de receptor de pantalla.</span><span class="sxs-lookup"><span data-stu-id="25869-108">The type of the display sink object.</span></span> <span data-ttu-id="25869-109">Puede usar el identificador predeterminado de **\_ tipo de \_ \_ objeto de \_ \_ receptor de visualización de WFD** , que se define como el valor 1.</span><span class="sxs-lookup"><span data-stu-id="25869-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="25869-110">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="25869-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="25869-111">Versión de revisión del objeto de receptor de pantalla.</span><span class="sxs-lookup"><span data-stu-id="25869-111">The revision version of the display sink object.</span></span> <span data-ttu-id="25869-112">Puede usar el identificador de la **revisión del objeto del receptor de visualización de la \_ \_ \_ \_ \_ versión \_ 1** del identificador, que se define como el valor 1.</span><span class="sxs-lookup"><span data-stu-id="25869-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="25869-113">**Duración**</span><span class="sxs-lookup"><span data-stu-id="25869-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="25869-114">La longitud de los datos en el resultado de notificación o notificación.</span><span class="sxs-lookup"><span data-stu-id="25869-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25869-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25869-115">Requirements</span></span>



| <span data-ttu-id="25869-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25869-116">Requirement</span></span> | <span data-ttu-id="25869-117">Value</span><span class="sxs-lookup"><span data-stu-id="25869-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25869-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25869-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25869-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="25869-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="25869-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25869-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25869-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25869-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="25869-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25869-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25869-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="25869-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




