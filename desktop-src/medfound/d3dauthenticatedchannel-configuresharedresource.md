---
description: Contiene datos de entrada para un \_ comando D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696158"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="0497f-103">D3DAUTHENTICATEDCHANNEL \_ estructura CONFIGURESHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="0497f-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="0497f-104">Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="0497f-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="0497f-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="0497f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="0497f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0497f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="0497f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0497f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0497f-108">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="0497f-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="0497f-109">[**D3DAUTHENTICATEDCHANNEL \_ configure \_**](d3dauthenticatedchannel-configure-input.md) la estructura de entrada que contiene el GUID del comando y otros datos.</span><span class="sxs-lookup"><span data-stu-id="0497f-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="0497f-110">**ProcessIdentiferType**</span><span class="sxs-lookup"><span data-stu-id="0497f-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="0497f-111">Un valor de [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) que especifica el tipo de proceso.</span><span class="sxs-lookup"><span data-stu-id="0497f-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="0497f-112">Para especificar el proceso de Administrador de ventanas de escritorio (DWM), establezca este miembro en **PROCESSIDTYPE \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="0497f-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="0497f-113">De lo contrario, establezca este miembro en **PROCESSIDTYPE \_ Handle** y establezca el miembro **ProcessHandle** en un identificador válido.</span><span class="sxs-lookup"><span data-stu-id="0497f-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="0497f-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="0497f-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="0497f-115">Identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="0497f-115">A process handle.</span></span> <span data-ttu-id="0497f-116">Si el miembro **ProcessIdentifier** es igual **al \_ identificador PROCESSTIDTYPE**, el miembro **ProcessHandle** especifica un identificador para un proceso.</span><span class="sxs-lookup"><span data-stu-id="0497f-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="0497f-117">De lo contrario, se omite el valor.</span><span class="sxs-lookup"><span data-stu-id="0497f-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="0497f-118">**AllowAccess**</span><span class="sxs-lookup"><span data-stu-id="0497f-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="0497f-119">Si **es true**, el proceso especificado tiene acceso a recursos compartidos restringidos.</span><span class="sxs-lookup"><span data-stu-id="0497f-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0497f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0497f-120">Requirements</span></span>



| <span data-ttu-id="0497f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0497f-121">Requirement</span></span> | <span data-ttu-id="0497f-122">Value</span><span class="sxs-lookup"><span data-stu-id="0497f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0497f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0497f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0497f-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0497f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0497f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0497f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0497f-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0497f-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0497f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0497f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0497f-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0497f-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0497f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0497f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0497f-130">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0497f-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0497f-131">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="0497f-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




