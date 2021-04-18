---
title: WMDRM_ENCRYPT_SCATTER_BLOCK estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de bloques de dispersión cifrada WMDRM contiene un bloque de datos que se van a cifrar.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721581"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="65611-105">\_Cifrado de la \_ estructura de bloques de dispersión de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="65611-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="65611-106">La estructura de **\_ \_ \_ bloques de dispersión cifrada WMDRM** contiene un bloque de datos que se van a cifrar.</span><span class="sxs-lookup"><span data-stu-id="65611-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="65611-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65611-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="65611-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="65611-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="65611-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="65611-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="65611-110">Identificador de la secuencia a la que pertenece el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="65611-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="65611-111">**cbBlock**</span><span class="sxs-lookup"><span data-stu-id="65611-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="65611-112">Tamaño del bloque en bytes.</span><span class="sxs-lookup"><span data-stu-id="65611-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="65611-113">**pbBlock**</span><span class="sxs-lookup"><span data-stu-id="65611-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="65611-114">Puntero a un búfer que contiene el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="65611-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65611-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65611-115">Remarks</span></span>

<span data-ttu-id="65611-116">El método [**IWMDRMEncryptScatter:: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) usa esta estructura para identificar los bloques de datos que se van a cifrar.</span><span class="sxs-lookup"><span data-stu-id="65611-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="65611-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65611-117">Requirements</span></span>



| <span data-ttu-id="65611-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65611-118">Requirement</span></span> | <span data-ttu-id="65611-119">Value</span><span class="sxs-lookup"><span data-stu-id="65611-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65611-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65611-120">Header</span></span><br/> | <dl> <span data-ttu-id="65611-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="65611-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65611-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="65611-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65611-123">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="65611-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





