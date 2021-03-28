---
description: Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando Undelete en el menú archivo.
title: FM_UNDELETE_PROC puntero a función (Wfext. h)
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
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278863"
---
# <a name="fm_undelete_proc-function-pointer"></a><span data-ttu-id="aebf5-103">\_Puntero de función de procedimiento de eliminación de FM \_</span><span class="sxs-lookup"><span data-stu-id="aebf5-103">FM\_UNDELETE\_PROC function pointer</span></span>

<span data-ttu-id="aebf5-104">Especifica una función de devolución de llamada definida por la aplicación llamada por el administrador de archivos cuando el usuario elige el comando **Undelete** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="aebf5-104">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="aebf5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aebf5-105">Syntax</span></span>


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a><span data-ttu-id="aebf5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aebf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebf5-107">*hwndOwner*</span><span class="sxs-lookup"><span data-stu-id="aebf5-107">*hwndOwner*</span></span> 
</dt> <dd>

<span data-ttu-id="aebf5-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="aebf5-108">Type: **HWND**</span></span>

<span data-ttu-id="aebf5-109">Identificador de ventana para el administrador de archivos.</span><span class="sxs-lookup"><span data-stu-id="aebf5-109">The window handle to File Manager.</span></span> <span data-ttu-id="aebf5-110">Un archivo DLL de deseliminación debe usar este identificador para especificar la ventana propietaria de cualquier cuadro de diálogo o cuadro de mensaje que el archivo DLL puede mostrar.</span><span class="sxs-lookup"><span data-stu-id="aebf5-110">An undelete DLL should use this handle to specify the owner window for any dialog box or message box the DLL might display.</span></span>

</dd> <dt>

<span data-ttu-id="aebf5-111">*lpszDir*</span><span class="sxs-lookup"><span data-stu-id="aebf5-111">*lpszDir*</span></span> 
</dt> <dd>

<span data-ttu-id="aebf5-112">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="aebf5-112">Type: **LPSTR**</span></span>

<span data-ttu-id="aebf5-113">Dirección de una cadena terminada en null que contiene el nombre del directorio inicial.</span><span class="sxs-lookup"><span data-stu-id="aebf5-113">The address of a null-terminated string that contains the name of the initial directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebf5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aebf5-114">Return value</span></span>

<span data-ttu-id="aebf5-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="aebf5-115">Type: **DWORD**</span></span>

<span data-ttu-id="aebf5-116">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="aebf5-116">Returns one of the following values.</span></span>



| <span data-ttu-id="aebf5-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aebf5-117">Return code</span></span>                                                                             | <span data-ttu-id="aebf5-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="aebf5-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="aebf5-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="aebf5-119"><dt>**-1**</dt></span></span> </dl>       | <span data-ttu-id="aebf5-120">Se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="aebf5-120">An error occurred.</span></span><br/>                                      |
| <dl> <span data-ttu-id="aebf5-121"><dt>**IDOK**</dt></span><span class="sxs-lookup"><span data-stu-id="aebf5-121"><dt>**IDOK**</dt></span></span> </dl>     | <span data-ttu-id="aebf5-122">Se ha cancelado la eliminación de un archivo.</span><span class="sxs-lookup"><span data-stu-id="aebf5-122">A file was undeleted.</span></span> <span data-ttu-id="aebf5-123">El administrador de archivos vuelve a dibujar su ventana.</span><span class="sxs-lookup"><span data-stu-id="aebf5-123">File Manager repaints its window.</span></span><br/> |
| <dl> <span data-ttu-id="aebf5-124"><dt>**IDCANCEL**</dt></span><span class="sxs-lookup"><span data-stu-id="aebf5-124"><dt>**IDCANCEL**</dt></span></span> </dl> | <span data-ttu-id="aebf5-125">No se eliminó ningún archivo.</span><span class="sxs-lookup"><span data-stu-id="aebf5-125">No file was undeleted.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="aebf5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aebf5-126">Requirements</span></span>



| <span data-ttu-id="aebf5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aebf5-127">Requirement</span></span> | <span data-ttu-id="aebf5-128">Value</span><span class="sxs-lookup"><span data-stu-id="aebf5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aebf5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebf5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aebf5-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="aebf5-130">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aebf5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aebf5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aebf5-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aebf5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aebf5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aebf5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="aebf5-134"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="aebf5-134"><dt>Wfext.h</dt></span></span> </dl> |



 

 




