---
title: WMDRM_IMPORT_CONTENT_KEY estructura (Drmexternals. h)
description: La \_ estructura de clave de contenido de importación de WMDRM \_ \_ almacena la clave de contenido que se usa en la importación de contenido protegido.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- WMDRM_IMPORT_CONTENT_KEY estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421979"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="33109-105">\_Estructura de \_ clave de contenido de importación de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="33109-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="33109-106">La estructura de clave de contenido de importación de WMDRM almacena la clave de contenido que se usa en la importación de contenido protegido. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="33109-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="33109-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33109-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="33109-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="33109-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33109-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="33109-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="33109-110">Se trata de la versión.</span><span class="sxs-lookup"><span data-stu-id="33109-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="33109-111">**cbStructSize**</span><span class="sxs-lookup"><span data-stu-id="33109-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="33109-112">Tamaño de la estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="33109-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33109-113">**dwIVKeyType**</span><span class="sxs-lookup"><span data-stu-id="33109-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="33109-114">Tipo de clave de vector de inicialización.</span><span class="sxs-lookup"><span data-stu-id="33109-114">Initialization vector key type.</span></span> <span data-ttu-id="33109-115">Establezca en WMDRM \_ KEYTYPE \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="33109-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="33109-116">**cbIVKey**</span><span class="sxs-lookup"><span data-stu-id="33109-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="33109-117">Tamaño de la clave de vector de inicialización en bytes.</span><span class="sxs-lookup"><span data-stu-id="33109-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33109-118">**dwContentKeyType**</span><span class="sxs-lookup"><span data-stu-id="33109-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="33109-119">Tipo de clave de contenido.</span><span class="sxs-lookup"><span data-stu-id="33109-119">Content key type.</span></span> <span data-ttu-id="33109-120">Establezca en el valor de cóctel del KEYTYPE de WMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="33109-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="33109-121">**cbContentKey**</span><span class="sxs-lookup"><span data-stu-id="33109-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="33109-122">Tamaño de la clave de contenido en bytes.</span><span class="sxs-lookup"><span data-stu-id="33109-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33109-123">**rgbKeyData**</span><span class="sxs-lookup"><span data-stu-id="33109-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="33109-124">Dirección de un búfer que contiene la clave de contenido.</span><span class="sxs-lookup"><span data-stu-id="33109-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="33109-125">El tamaño del búfer debe coincidir con el valor de **cbContentKey**.</span><span class="sxs-lookup"><span data-stu-id="33109-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="33109-126">Esta clave debe coincidir con la clave importada del mensaje de licencia de XMR.</span><span class="sxs-lookup"><span data-stu-id="33109-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33109-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33109-127">Remarks</span></span>

<span data-ttu-id="33109-128">Esta estructura, incluido el búfer que contiene la clave de sesión, se debe cifrar con la clave de sesión e incluirse en el miembro **pbEncryptedKeyMessage** de la estructura de la estructura de la estructura de [**importación de WMDRM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="33109-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="33109-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33109-129">Requirements</span></span>



| <span data-ttu-id="33109-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="33109-130">Requirement</span></span> | <span data-ttu-id="33109-131">Value</span><span class="sxs-lookup"><span data-stu-id="33109-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="33109-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33109-132">Minimum supported client</span></span><br/> | <span data-ttu-id="33109-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="33109-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="33109-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33109-134">Minimum supported server</span></span><br/> | <span data-ttu-id="33109-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="33109-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="33109-136">Versión</span><span class="sxs-lookup"><span data-stu-id="33109-136">Version</span></span><br/>                  | <span data-ttu-id="33109-137">SDK de Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="33109-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="33109-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33109-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="33109-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="33109-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33109-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="33109-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33109-141">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="33109-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





