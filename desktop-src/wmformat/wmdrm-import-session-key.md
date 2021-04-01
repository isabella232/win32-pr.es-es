---
title: WMDRM_IMPORT_SESSION_KEY estructura (Drmexternals. h)
description: La \_ \_ \_ estructura de la clave de sesión de importación de WMDRM contiene la clave de sesión para importar contenido protegido.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- WMDRM_IMPORT_SESSION_KEY estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150827"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="6c5ce-105">\_Estructura de \_ claves de sesión de importación de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="6c5ce-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="6c5ce-106">La estructura de la clave de sesión de importación de WMDRM contiene la clave de sesión para importar contenido protegido. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c5ce-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c5ce-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="6c5ce-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c5ce-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c5ce-109">**dwKeyType**</span><span class="sxs-lookup"><span data-stu-id="6c5ce-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="6c5ce-110">Tipo de clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-110">Session key type.</span></span> <span data-ttu-id="6c5ce-111">Establezca en WMDRM \_ KEYTYPE \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="6c5ce-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="6c5ce-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="6c5ce-113">Tamaño de la clave de sesión, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="6c5ce-114">Este valor puede ser tan grande como sea necesario, dados los límites de una única operación de RSA OAEP en todo el mensaje (esta estructura más la clave de sesión).</span><span class="sxs-lookup"><span data-stu-id="6c5ce-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="6c5ce-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="6c5ce-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="6c5ce-116">Dirección de un búfer que contiene la clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="6c5ce-117">El tamaño del búfer debe coincidir con el valor de **cbKey**.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="6c5ce-118">Los datos del búfer son un valor de clave generado aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="6c5ce-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c5ce-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c5ce-119">Remarks</span></span>

<span data-ttu-id="6c5ce-120">Esta estructura, incluido el búfer que contiene la clave de sesión, se debe cifrar con la clave pública de la máquina DRM de Windows Media e incluirse en el miembro **pbEncryptedSessionKeyMessage** de la estructura de la estructura de [**\_ \_ inicialización \_ de la importación WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="6c5ce-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5ce-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5ce-121">Requirements</span></span>



| <span data-ttu-id="6c5ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5ce-122">Requirement</span></span> | <span data-ttu-id="6c5ce-123">Value</span><span class="sxs-lookup"><span data-stu-id="6c5ce-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5ce-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5ce-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6c5ce-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6c5ce-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c5ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5ce-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c5ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6c5ce-128">Versión</span><span class="sxs-lookup"><span data-stu-id="6c5ce-128">Version</span></span><br/>                  | <span data-ttu-id="6c5ce-129">SDK de Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="6c5ce-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="6c5ce-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c5ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5ce-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5ce-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5ce-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c5ce-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5ce-133">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="6c5ce-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





