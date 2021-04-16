---
description: Deshabilita las características de.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650132"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="b81e9-103">pSetupSetGlobalFlags función)</span><span class="sxs-lookup"><span data-stu-id="b81e9-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="b81e9-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="b81e9-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="b81e9-105">Deshabilita las características de.</span><span class="sxs-lookup"><span data-stu-id="b81e9-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81e9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b81e9-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="b81e9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b81e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b81e9-108">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b81e9-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b81e9-109">Marcas usadas para deshabilitar la interfaz de usuario o la copia de seguridad automática.</span><span class="sxs-lookup"><span data-stu-id="b81e9-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="b81e9-110">Value</span><span class="sxs-lookup"><span data-stu-id="b81e9-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="b81e9-111">Significado</span><span class="sxs-lookup"><span data-stu-id="b81e9-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="b81e9-112"><dt>**PSPGF \_**</dt> <dt>0x004</dt> no interactivo</span><span class="sxs-lookup"><span data-stu-id="b81e9-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="b81e9-113">Establezca en deshabilitar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b81e9-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="b81e9-114"><dt>**PSPGF \_ SIN \_**</dt> <dt>0x002</dt> de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="b81e9-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="b81e9-115">Establezca esta configuración en deshabilitar copia de seguridad automática.</span><span class="sxs-lookup"><span data-stu-id="b81e9-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b81e9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b81e9-116">Return value</span></span>

<span data-ttu-id="b81e9-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b81e9-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b81e9-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b81e9-118">Remarks</span></span>

<span data-ttu-id="b81e9-119">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b81e9-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81e9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b81e9-120">Requirements</span></span>



| <span data-ttu-id="b81e9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81e9-121">Requirement</span></span> | <span data-ttu-id="b81e9-122">Value</span><span class="sxs-lookup"><span data-stu-id="b81e9-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e9-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b81e9-123">DLL</span></span><br/> | <dl> <span data-ttu-id="b81e9-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b81e9-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
