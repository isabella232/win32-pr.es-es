---
title: Método INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Lo implementan los validadores de mantenimiento del sistema (SHV) según sea necesario para administrar la configuración remota directamente en el equipo especificado. Este método inicia una interfaz de usuario de administración de configuración.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Método InvokeUIForMachine NAP
- Método InvokeUIForMachine NAP, interfaz INapComponentConfig2
- Interfaz INapComponentConfig2 NAP, método InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150223"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="9185b-107">INapComponentConfig2:: InvokeUIForMachine (método)</span><span class="sxs-lookup"><span data-stu-id="9185b-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="9185b-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="9185b-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9185b-109">Los validadores de mantenimiento del sistema (SHV) implementan el método **InvokeUIForMachine** según sea necesario para administrar la configuración remota directamente en el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="9185b-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="9185b-110">Este método inicia una interfaz de usuario de administración de configuración.</span><span class="sxs-lookup"><span data-stu-id="9185b-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="9185b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9185b-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="9185b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9185b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9185b-113">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9185b-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9185b-114">Identificador de la ventana primaria o propietaria.</span><span class="sxs-lookup"><span data-stu-id="9185b-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="9185b-115">Se debe proporcionar un identificador de ventana válido.</span><span class="sxs-lookup"><span data-stu-id="9185b-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="9185b-116">*MachineName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9185b-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9185b-117">Un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contiene el nombre de equipo del cliente NAP.</span><span class="sxs-lookup"><span data-stu-id="9185b-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9185b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9185b-118">Return value</span></span>

<span data-ttu-id="9185b-119">Devuelve \_ si es correcto, o uno de los códigos de error estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="9185b-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9185b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9185b-120">Requirements</span></span>



| <span data-ttu-id="9185b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9185b-121">Requirement</span></span> | <span data-ttu-id="9185b-122">Value</span><span class="sxs-lookup"><span data-stu-id="9185b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9185b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9185b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9185b-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9185b-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9185b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9185b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9185b-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9185b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9185b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9185b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9185b-128"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9185b-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9185b-129">IDL</span><span class="sxs-lookup"><span data-stu-id="9185b-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9185b-130"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9185b-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9185b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9185b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9185b-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="9185b-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





