---
description: Contiene información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).
title: FMS_GETFILESEL estructura (Wfext. h)
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
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000858"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="8d360-103">Estructura de FMS \_ GETFILESEL</span><span class="sxs-lookup"><span data-stu-id="8d360-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="8d360-104">Contiene información sobre un archivo seleccionado en la ventana del administrador de archivos activo (la ventana Directorio o la ventana Resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="8d360-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d360-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d360-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="8d360-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d360-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d360-107">**ftTime**</span><span class="sxs-lookup"><span data-stu-id="8d360-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="8d360-108">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="8d360-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="8d360-109">Fecha y hora en que se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="8d360-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="8d360-110">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="8d360-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="8d360-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8d360-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8d360-112">Tamaño, en bytes, del archivo.</span><span class="sxs-lookup"><span data-stu-id="8d360-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8d360-113">**Bater**</span><span class="sxs-lookup"><span data-stu-id="8d360-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="8d360-114">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="8d360-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="8d360-115">Atributos del archivo.</span><span class="sxs-lookup"><span data-stu-id="8d360-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8d360-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="8d360-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="8d360-117">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="8d360-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="8d360-118">La ruta de acceso completa y el nombre de archivo del archivo seleccionado terminados en NULL.</span><span class="sxs-lookup"><span data-stu-id="8d360-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d360-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d360-119">Requirements</span></span>



| <span data-ttu-id="8d360-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d360-120">Requirement</span></span> | <span data-ttu-id="8d360-121">Value</span><span class="sxs-lookup"><span data-stu-id="8d360-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d360-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d360-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d360-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8d360-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8d360-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d360-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d360-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d360-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8d360-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d360-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d360-127"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d360-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d360-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d360-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d360-129">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="8d360-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




