---
description: Inicializa el administrador de componentes opcional.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649627"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="9ac85-103">OcInitialize función)</span><span class="sxs-lookup"><span data-stu-id="9ac85-103">OcInitialize function</span></span>

<span data-ttu-id="9ac85-104">Inicializa el administrador de componentes opcional.</span><span class="sxs-lookup"><span data-stu-id="9ac85-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac85-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ac85-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="9ac85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ac85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac85-107">*Devoluciones de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ac85-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac85-108">Puntero a una estructura [**de \_ \_ devoluciones de llamada de cliente de OCM**](ocm-client-callbacks.md) que especifica las funciones de devolución de llamada que va a usar el administrador de OC para realizar varias tareas.</span><span class="sxs-lookup"><span data-stu-id="9ac85-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="9ac85-109">*MasterOcInfName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9ac85-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac85-110">Ruta de acceso del archivo. inf de procesamiento maestro.</span><span class="sxs-lookup"><span data-stu-id="9ac85-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="9ac85-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9ac85-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac85-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ac85-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9ac85-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9ac85-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="9ac85-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9ac85-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="9ac85-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9ac85-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="9ac85-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9ac85-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9ac85-117">*ShowError* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9ac85-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac85-118">Si se produce un error en la función, este parámetro indica si se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="9ac85-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="9ac85-119">*Registro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9ac85-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac85-120">Identificador del registro.</span><span class="sxs-lookup"><span data-stu-id="9ac85-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac85-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ac85-121">Return value</span></span>

<span data-ttu-id="9ac85-122">La función devuelve el valor de contexto del administrador de OC.</span><span class="sxs-lookup"><span data-stu-id="9ac85-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ac85-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ac85-123">Remarks</span></span>

<span data-ttu-id="9ac85-124">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9ac85-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac85-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ac85-125">Requirements</span></span>



| <span data-ttu-id="9ac85-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac85-126">Requirement</span></span> | <span data-ttu-id="9ac85-127">Value</span><span class="sxs-lookup"><span data-stu-id="9ac85-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac85-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ac85-128">DLL</span></span><br/> | <dl> <span data-ttu-id="9ac85-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ac85-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac85-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ac85-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac85-131">**\_devoluciones de llamada de cliente de OCM \_**</span><span class="sxs-lookup"><span data-stu-id="9ac85-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="9ac85-132">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="9ac85-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
