---
description: Registra los servicios de Intercambio dinámico de datos de Shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985882"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="7e13a-103">ShellDDEInit función)</span><span class="sxs-lookup"><span data-stu-id="7e13a-103">ShellDDEInit function</span></span>

<span data-ttu-id="7e13a-104">Registra los servicios de Intercambio dinámico de datos de Shell (DDE) en el proceso actual, notificando al sistema que el proceso actual desea hospedar objetos DDE.</span><span class="sxs-lookup"><span data-stu-id="7e13a-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e13a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e13a-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="7e13a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e13a-107">*init* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e13a-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e13a-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="7e13a-108">Type: **BOOL**</span></span>

<span data-ttu-id="7e13a-109">**True** para registrar el proceso actual como host DDE; **False** para anular el registro.</span><span class="sxs-lookup"><span data-stu-id="7e13a-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e13a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e13a-110">Return value</span></span>

<span data-ttu-id="7e13a-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7e13a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e13a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e13a-112">Remarks</span></span>

<span data-ttu-id="7e13a-113">El proceso que llama a esta función actúa como el Shell y se usa para ver el contenido de las carpetas abiertas con el verbo ' Open ' de [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="7e13a-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="7e13a-114">Esta función no tiene un archivo de encabezado o biblioteca asociado, por lo que debe llamarse por valor ordinal.</span><span class="sxs-lookup"><span data-stu-id="7e13a-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="7e13a-115">Llame a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con el nombre del archivo DLL (Shdocvw.dll) para obtener un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="7e13a-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="7e13a-116">A continuación, llame a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con ese identificador de módulo y el número ordinal de función 118 para obtener la dirección de la función.</span><span class="sxs-lookup"><span data-stu-id="7e13a-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e13a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e13a-117">Requirements</span></span>



| <span data-ttu-id="7e13a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e13a-118">Requirement</span></span> | <span data-ttu-id="7e13a-119">Value</span><span class="sxs-lookup"><span data-stu-id="7e13a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e13a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e13a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e13a-121">Solo aplicaciones de escritorio de Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="7e13a-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e13a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e13a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e13a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e13a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7e13a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e13a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e13a-125"><dt>Shdocvw.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7e13a-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
