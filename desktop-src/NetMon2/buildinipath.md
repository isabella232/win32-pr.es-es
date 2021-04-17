---
description: La función BuildINIPath devuelve una ruta de acceso completa a un archivo INI que corresponde a la información que especifique.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Función BuildINIPath (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667743"
---
# <a name="buildinipath-function"></a><span data-ttu-id="bb94b-103">BuildINIPath función)</span><span class="sxs-lookup"><span data-stu-id="bb94b-103">BuildINIPath function</span></span>

<span data-ttu-id="bb94b-104">La función **BuildINIPath** devuelve una ruta de acceso completa a un archivo ini que corresponde a la información que especifique.</span><span class="sxs-lookup"><span data-stu-id="bb94b-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb94b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb94b-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="bb94b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb94b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb94b-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="bb94b-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="bb94b-108">Búfer que recibe el nombre de archivo INI completo.</span><span class="sxs-lookup"><span data-stu-id="bb94b-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="bb94b-109">*IniFileName*</span><span class="sxs-lookup"><span data-stu-id="bb94b-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="bb94b-110">Nombre del archivo INI (el nombre de archivo completo menos la extensión de nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="bb94b-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb94b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb94b-111">Return value</span></span>

<span data-ttu-id="bb94b-112">Si la función se realiza correctamente, el valor devuelto es un puntero al nombre de archivo INI completo.</span><span class="sxs-lookup"><span data-stu-id="bb94b-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="bb94b-113">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="bb94b-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb94b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb94b-114">Remarks</span></span>

<span data-ttu-id="bb94b-115">La ruta de acceso que devuelve esta función es una ruta de acceso completa a un archivo INI que corresponde a la información especificada.</span><span class="sxs-lookup"><span data-stu-id="bb94b-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="bb94b-116">Por ejemplo, si especifica XNS o TCP, la función genera una ruta de acceso a Xns.ini o Tcp.ini, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bb94b-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb94b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb94b-117">Requirements</span></span>



| <span data-ttu-id="bb94b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb94b-118">Requirement</span></span> | <span data-ttu-id="bb94b-119">Value</span><span class="sxs-lookup"><span data-stu-id="bb94b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb94b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb94b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb94b-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb94b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bb94b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb94b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb94b-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb94b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb94b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb94b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb94b-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb94b-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb94b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb94b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb94b-127"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb94b-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb94b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb94b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb94b-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb94b-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




