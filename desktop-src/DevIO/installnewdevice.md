---
description: Instala un nuevo dispositivo. Se solicita al usuario que seleccione el dispositivo.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153332"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="2b809-104">InstallNewDevice función)</span><span class="sxs-lookup"><span data-stu-id="2b809-104">InstallNewDevice function</span></span>

<span data-ttu-id="2b809-105">Instala un nuevo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b809-105">Installs a new device.</span></span> <span data-ttu-id="2b809-106">Se solicita al usuario que seleccione el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b809-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b809-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b809-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="2b809-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b809-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b809-109">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b809-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b809-110">Identificador de la ventana de nivel superior que se va a usar para cualquier interfaz de usuario necesaria.</span><span class="sxs-lookup"><span data-stu-id="2b809-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="2b809-111">*ClassGuid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b809-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b809-112">Un puntero a un **GUID** de clase.</span><span class="sxs-lookup"><span data-stu-id="2b809-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="2b809-113">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="2b809-113">This parameter is optional.</span></span> <span data-ttu-id="2b809-114">Si este parámetro es **null**, el usuario se inicia en la página de opciones de detección.</span><span class="sxs-lookup"><span data-stu-id="2b809-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="2b809-115">Si este parámetro es **GUID \_ null** o **GUID \_ DEVCLASS \_ Unknown**, el usuario se inicia en la página de selección de clases.</span><span class="sxs-lookup"><span data-stu-id="2b809-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="2b809-116">*Inicio previo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2b809-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b809-117">Un puntero a una variable que recibe el estado de reinicio.</span><span class="sxs-lookup"><span data-stu-id="2b809-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="2b809-118">Este parámetro puede ser **di \_ NEEDRESTART** o **di \_ NEEDREBOOT**.</span><span class="sxs-lookup"><span data-stu-id="2b809-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b809-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b809-119">Return value</span></span>

<span data-ttu-id="2b809-120">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2b809-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="2b809-121">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="2b809-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="2b809-122">Para obtener información de error extendida, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2b809-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="2b809-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b809-123">Remarks</span></span>

<span data-ttu-id="2b809-124">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="2b809-124">This function has no associated import library.</span></span> <span data-ttu-id="2b809-125">Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a NewDev.dll.</span><span class="sxs-lookup"><span data-stu-id="2b809-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b809-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b809-126">Requirements</span></span>



| <span data-ttu-id="2b809-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b809-127">Requirement</span></span> | <span data-ttu-id="2b809-128">Value</span><span class="sxs-lookup"><span data-stu-id="2b809-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b809-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b809-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b809-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2b809-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="2b809-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b809-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b809-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b809-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="2b809-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b809-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b809-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b809-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b809-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b809-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b809-136">Funciones de administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="2b809-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

