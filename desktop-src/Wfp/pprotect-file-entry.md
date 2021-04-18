---
description: Estructura utilizada por la función SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY estructura (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706395"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="a6173-103">PPROTECT \_ estructura de entrada de archivo \_</span><span class="sxs-lookup"><span data-stu-id="a6173-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="a6173-104">\[Esta estructura está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a6173-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6173-105">Se ha quitado la compatibilidad con esta estructura en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a6173-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a6173-106">En su lugar, use las funciones admitidas que se enumeran en [las funciones de WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="a6173-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="a6173-107">Estructura utilizada por la función [**SfcGetFiles**](sfcgetfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="a6173-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6173-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6173-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="a6173-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6173-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6173-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="a6173-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="a6173-111">Puntero a un valor de cadena que contiene el nombre de archivo del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a6173-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="a6173-112">Será **null** si no se cambia el nombre del archivo durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="a6173-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="a6173-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a6173-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="a6173-114">Puntero al valor de cadena que contiene el nombre de archivo de destino más la ruta de acceso completa al archivo.</span><span class="sxs-lookup"><span data-stu-id="a6173-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="a6173-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="a6173-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="a6173-116">Puntero al valor de cadena que contiene el nombre del archivo INF que proporciona información de diseño.</span><span class="sxs-lookup"><span data-stu-id="a6173-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="a6173-117">Este parámetro puede ser **null** cuando se usa el diseño predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6173-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6173-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6173-118">Requirements</span></span>



| <span data-ttu-id="a6173-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6173-119">Requirement</span></span> | <span data-ttu-id="a6173-120">Value</span><span class="sxs-lookup"><span data-stu-id="a6173-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6173-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6173-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6173-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a6173-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6173-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6173-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6173-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6173-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6173-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a6173-125">End of client support</span></span><br/>    | <span data-ttu-id="a6173-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6173-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="a6173-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a6173-127">End of server support</span></span><br/>    | <span data-ttu-id="a6173-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6173-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="a6173-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6173-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6173-130"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6173-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6173-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6173-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6173-132">**SfcGetFiles**</span><span class="sxs-lookup"><span data-stu-id="a6173-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




