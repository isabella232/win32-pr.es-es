---
description: La función InstallWiaDevice instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo raíz enumerado. Puede mostrar una advertencia de seguridad si algún archivo o Coinstalador de instalación no está firmado digitalmente y es de confianza.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Función InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810796"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="b21b5-104">InstallWiaDevice función)</span><span class="sxs-lookup"><span data-stu-id="b21b5-104">InstallWiaDevice function</span></span>

<span data-ttu-id="b21b5-105">La función **InstallWiaDevice** instala un dispositivo de adquisición de imágenes de Windows (WIA) como dispositivo raíz enumerado.</span><span class="sxs-lookup"><span data-stu-id="b21b5-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="b21b5-106">Puede mostrar una advertencia de seguridad si algún archivo o Coinstalador de instalación no está firmado digitalmente y es de confianza.</span><span class="sxs-lookup"><span data-stu-id="b21b5-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b21b5-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="b21b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b21b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21b5-109">*pWiaDeviceInstall* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b21b5-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21b5-110">Tipo: \**PWIADEVICEINSTALL \** _</span><span class="sxs-lookup"><span data-stu-id="b21b5-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="b21b5-111">Puntero a una estructura WIADEVICEINSTALL.</span><span class="sxs-lookup"><span data-stu-id="b21b5-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="b21b5-112">El miembro _szFriendlyName \* de la estructura se debe establecer en el dispositivo FriendlyName real.</span><span class="sxs-lookup"><span data-stu-id="b21b5-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21b5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b21b5-113">Return value</span></span>

<span data-ttu-id="b21b5-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b21b5-114">Type: **DWORD**</span></span>

<span data-ttu-id="b21b5-115">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b21b5-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b21b5-116">Si se produce un error en la función, devuelve un código de error de Win32.</span><span class="sxs-lookup"><span data-stu-id="b21b5-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21b5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b21b5-117">Requirements</span></span>



| <span data-ttu-id="b21b5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b21b5-118">Requirement</span></span> | <span data-ttu-id="b21b5-119">Value</span><span class="sxs-lookup"><span data-stu-id="b21b5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b21b5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b21b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b21b5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b21b5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b21b5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b21b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b21b5-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b21b5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b21b5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b21b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b21b5-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b21b5-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b21b5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b21b5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b21b5-127"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b21b5-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




