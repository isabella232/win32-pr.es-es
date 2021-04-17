---
title: Estructura VarFileInfo
description: Representa la organización de los datos en un recurso de versión de archivo. Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Menús de la estructura VarFileInfo y otros recursos
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714609"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="f0f2b-105">Estructura VarFileInfo</span><span class="sxs-lookup"><span data-stu-id="f0f2b-105">VarFileInfo structure</span></span>

<span data-ttu-id="f0f2b-106">Representa la organización de los datos en un recurso de versión de archivo.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="f0f2b-107">Contiene información de versión que no depende de una combinación de idioma y página de códigos determinada.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f2b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0f2b-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="f0f2b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0f2b-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0f2b-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-112">La longitud, en bytes, del bloque **VarFileInfo** completo, incluidas todas las estructuras indicadas por el miembro **secundario** .</span><span class="sxs-lookup"><span data-stu-id="f0f2b-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="f0f2b-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-115">Este miembro siempre es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0f2b-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-118">El tipo de datos del recurso de versión.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-118">The type of data in the version resource.</span></span> <span data-ttu-id="f0f2b-119">Este miembro es 1 si el recurso de versión contiene datos de texto y 0 si el recurso de versión contiene datos binarios.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="f0f2b-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-121">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-122">Cadena Unicode L "VarFileInfo".</span><span class="sxs-lookup"><span data-stu-id="f0f2b-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="f0f2b-123">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-125">Tantas palabras como sea necesario para alinear el miembro **secundario** en un límite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="f0f2b-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="f0f2b-127">Tipo: **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f0f2b-128">Normalmente contiene una lista de idiomas compatibles con la aplicación o el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0f2b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0f2b-129">Remarks</span></span>

<span data-ttu-id="f0f2b-130">Esta estructura no es una estructura de lenguaje C verdadera porque contiene miembros de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="f0f2b-131">Esta estructura se creó únicamente para representar la organización de los datos en un recurso de versión y no aparece en ninguno de los archivos de encabezado incluidos en el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="f0f2b-132">El miembro **secundario** de la estructura de [**vs \_ versionInfo**](vs-versioninfo.md) puede contener cero o una estructura **VarFileInfo** .</span><span class="sxs-lookup"><span data-stu-id="f0f2b-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f2b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0f2b-133">Requirements</span></span>



| <span data-ttu-id="f0f2b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0f2b-134">Requirement</span></span> | <span data-ttu-id="f0f2b-135">Value</span><span class="sxs-lookup"><span data-stu-id="f0f2b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f0f2b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0f2b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f0f2b-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f0f2b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f0f2b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0f2b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f0f2b-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0f2b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f0f2b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0f2b-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0f2b-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0f2b-142">**Distribuidor**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="f0f2b-143">**VS \_ versionInfo**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="f0f2b-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f0f2b-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f0f2b-145">Información de versión</span><span class="sxs-lookup"><span data-stu-id="f0f2b-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





