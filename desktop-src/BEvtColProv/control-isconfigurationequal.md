---
description: Compare el argumento con la configuración activa del recopilador.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Método IsConfigurationEqual de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806991"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="204db-103">Método IsConfigurationEqual de la clase control</span><span class="sxs-lookup"><span data-stu-id="204db-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="204db-104">Compare el argumento con la configuración activa del recopilador.</span><span class="sxs-lookup"><span data-stu-id="204db-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="204db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="204db-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="204db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="204db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="204db-107">*Configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="204db-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="204db-108">Configuración que se va a comparar con la configuración activa.</span><span class="sxs-lookup"><span data-stu-id="204db-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="204db-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="204db-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="204db-110">0</span><span class="sxs-lookup"><span data-stu-id="204db-110">0</span></span>

<span data-ttu-id="204db-111">Error</span><span class="sxs-lookup"><span data-stu-id="204db-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="204db-112">1</span><span class="sxs-lookup"><span data-stu-id="204db-112">1</span></span>

<span data-ttu-id="204db-113">Correcto</span><span class="sxs-lookup"><span data-stu-id="204db-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="204db-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="204db-114">Requirements</span></span>



| <span data-ttu-id="204db-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="204db-115">Requirement</span></span> | <span data-ttu-id="204db-116">Value</span><span class="sxs-lookup"><span data-stu-id="204db-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="204db-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="204db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="204db-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="204db-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="204db-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="204db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="204db-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="204db-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="204db-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="204db-121">Namespace</span></span><br/>                | <span data-ttu-id="204db-122">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="204db-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="204db-123">MOF</span><span class="sxs-lookup"><span data-stu-id="204db-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="204db-124"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="204db-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="204db-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="204db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="204db-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="204db-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="204db-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="204db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204db-128">**Control**</span><span class="sxs-lookup"><span data-stu-id="204db-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




