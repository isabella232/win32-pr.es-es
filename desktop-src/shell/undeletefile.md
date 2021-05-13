---
description: Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos cuando el usuario elige el comando Undelete en el menú Archivo.
title: FM_UNDELETE_PROC de función (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842426"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="360c8-103">Puntero \_ de función FM UNDELETE \_ PROC</span><span class="sxs-lookup"><span data-stu-id="360c8-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="360c8-104">Especifica una función de devolución de llamada definida por la aplicación a la que llama el Administrador de archivos cuando el usuario elige el comando **Undelete** en el **menú** Archivo.</span><span class="sxs-lookup"><span data-stu-id="360c8-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="360c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="360c8-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="360c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="360c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360c8-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="360c8-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="360c8-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="360c8-108">Type: **HWND**</span></span>

<span data-ttu-id="360c8-109">Identificador de ventana del Administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="360c8-109">The window handle to File Manager.</span></span> <span data-ttu-id="360c8-110">Un archivo DLL de recuperación debe usar este identificador para especificar la ventana de propietario de cualquier cuadro de diálogo o cuadro de mensaje que pueda mostrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="360c8-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="360c8-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="360c8-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="360c8-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="360c8-112">Type: **LPSTR**</span></span>

<span data-ttu-id="360c8-113">Dirección de una cadena terminada en NULL que contiene el nombre del directorio inicial.</span><span class="sxs-lookup"><span data-stu-id="360c8-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360c8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="360c8-114">Return value</span></span>

<span data-ttu-id="360c8-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="360c8-115">Type: **DWORD**</span></span>

<span data-ttu-id="360c8-116">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="360c8-116">Returns one of the following values.</span></span>



| <span data-ttu-id="360c8-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="360c8-117">Return code</span></span>                                                                             | <span data-ttu-id="360c8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="360c8-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="360c8-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="360c8-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="360c8-120">Se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="360c8-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="360c8-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="360c8-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="360c8-122">Se ha eliminado un archivo.</span><span class="sxs-lookup"><span data-stu-id="360c8-122">A file was undeleted.</span></span> <span data-ttu-id="360c8-123">El Administrador de archivos vuelve a dibujar su ventana.</span><span class="sxs-lookup"><span data-stu-id="360c8-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="360c8-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="360c8-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="360c8-125">No se ha eliminado ningún archivo.</span><span class="sxs-lookup"><span data-stu-id="360c8-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="360c8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="360c8-126">Requirements</span></span>



| <span data-ttu-id="360c8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="360c8-127">Requirement</span></span> | <span data-ttu-id="360c8-128">Value</span><span class="sxs-lookup"><span data-stu-id="360c8-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="360c8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="360c8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="360c8-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="360c8-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="360c8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="360c8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="360c8-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="360c8-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="360c8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="360c8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="360c8-134"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="360c8-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




