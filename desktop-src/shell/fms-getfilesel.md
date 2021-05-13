---
description: Contiene información sobre un archivo seleccionado en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).
title: FMS_GETFILESEL estructura (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842226"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="474ce-103">FMS \_ GETFILESEL (estructura)</span><span class="sxs-lookup"><span data-stu-id="474ce-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="474ce-104">Contiene información sobre un archivo seleccionado en la ventana activa del Administrador de archivos (la ventana de directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="474ce-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="474ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="474ce-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="474ce-106">Members</span><span class="sxs-lookup"><span data-stu-id="474ce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="474ce-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="474ce-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="474ce-108">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="474ce-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="474ce-109">Hora y fecha en que se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="474ce-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="474ce-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="474ce-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="474ce-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="474ce-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="474ce-112">Tamaño, en bytes, del archivo.</span><span class="sxs-lookup"><span data-stu-id="474ce-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="474ce-113">**bAttr**</span><span class="sxs-lookup"><span data-stu-id="474ce-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="474ce-114">Tipo: **BYTE**</span><span class="sxs-lookup"><span data-stu-id="474ce-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="474ce-115">Atributos del archivo.</span><span class="sxs-lookup"><span data-stu-id="474ce-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="474ce-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="474ce-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="474ce-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="474ce-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="474ce-118">Ruta de acceso completa terminada en NULL y nombre de archivo del archivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="474ce-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="474ce-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="474ce-119">Requirements</span></span>



| <span data-ttu-id="474ce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="474ce-120">Requirement</span></span> | <span data-ttu-id="474ce-121">Value</span><span class="sxs-lookup"><span data-stu-id="474ce-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="474ce-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="474ce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="474ce-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="474ce-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="474ce-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="474ce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="474ce-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="474ce-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="474ce-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="474ce-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="474ce-127"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="474ce-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="474ce-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="474ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474ce-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="474ce-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




