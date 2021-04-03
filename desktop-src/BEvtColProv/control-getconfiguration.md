---
description: Lea la configuración activa del recopilador.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Método GetConfiguration de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998084"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="82b19-103">Método GetConfiguration de la clase control</span><span class="sxs-lookup"><span data-stu-id="82b19-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="82b19-104">Lea la configuración activa del recopilador.</span><span class="sxs-lookup"><span data-stu-id="82b19-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82b19-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="82b19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b19-107">*TimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82b19-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82b19-108">Cuando este método finaliza, este parámetro contiene los bits de orden inferior de una marca de tiempo que indica cuándo se estableció la configuración.</span><span class="sxs-lookup"><span data-stu-id="82b19-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="82b19-109">*TimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="82b19-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82b19-110">Cuando este método finaliza, este parámetro contiene los bits de orden superior de una marca de tiempo que indica cuándo se estableció la configuración.</span><span class="sxs-lookup"><span data-stu-id="82b19-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b19-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82b19-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="82b19-112">0</span><span class="sxs-lookup"><span data-stu-id="82b19-112">0</span></span>

<span data-ttu-id="82b19-113">Error</span><span class="sxs-lookup"><span data-stu-id="82b19-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="82b19-114">1</span><span class="sxs-lookup"><span data-stu-id="82b19-114">1</span></span>

<span data-ttu-id="82b19-115">Correcto</span><span class="sxs-lookup"><span data-stu-id="82b19-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82b19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b19-116">Requirements</span></span>



| <span data-ttu-id="82b19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b19-117">Requirement</span></span> | <span data-ttu-id="82b19-118">Value</span><span class="sxs-lookup"><span data-stu-id="82b19-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b19-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82b19-120">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="82b19-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="82b19-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82b19-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82b19-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="82b19-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82b19-123">Namespace</span></span><br/>                | <span data-ttu-id="82b19-124">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="82b19-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="82b19-125">MOF</span><span class="sxs-lookup"><span data-stu-id="82b19-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82b19-126"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82b19-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="82b19-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82b19-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82b19-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82b19-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="82b19-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="82b19-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b19-130">**Control**</span><span class="sxs-lookup"><span data-stu-id="82b19-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




