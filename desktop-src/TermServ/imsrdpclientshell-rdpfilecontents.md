---
title: Propiedad RdpFileContents de IMsRdpClientShell
description: Especifica o recupera el contenido del archivo Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otro portal web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RdpFileContents
- Propiedad RdpFileContents Servicios de Escritorio remoto, interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, propiedad RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686068"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="d7331-106">IMsRdpClientShell:: RdpFileContents (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d7331-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="d7331-107">Especifica o recupera el contenido del archivo Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otro portal web.</span><span class="sxs-lookup"><span data-stu-id="d7331-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="d7331-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d7331-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7331-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7331-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="d7331-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d7331-110">Property value</span></span>

<span data-ttu-id="d7331-111">Especifica el contenido del archivo RDP que se va a iniciar desde el portal web.</span><span class="sxs-lookup"><span data-stu-id="d7331-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7331-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7331-112">Requirements</span></span>



| <span data-ttu-id="d7331-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7331-113">Requirement</span></span> | <span data-ttu-id="d7331-114">Value</span><span class="sxs-lookup"><span data-stu-id="d7331-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7331-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7331-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d7331-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7331-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d7331-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7331-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d7331-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7331-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d7331-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d7331-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7331-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7331-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7331-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7331-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7331-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7331-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7331-123">IID</span><span class="sxs-lookup"><span data-stu-id="d7331-123">IID</span></span><br/>                      | <span data-ttu-id="d7331-124">IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="d7331-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d7331-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7331-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7331-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="d7331-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





