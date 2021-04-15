---
description: Define una matriz de cuantificación.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC estructura (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539562"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="77835-103">Qmatrix de DXVA \_ \_ HEVC estructura</span><span class="sxs-lookup"><span data-stu-id="77835-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="77835-104">Define una matriz de cuantificación.</span><span class="sxs-lookup"><span data-stu-id="77835-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="77835-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77835-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="77835-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="77835-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="77835-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="77835-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="77835-108">Contiene las listas de escalado para el proceso de escala de 4x4, correspondiente a ScalingList \[ 0 \] \[ MatrixID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, e i está en el intervalo de 0 a 15, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="77835-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="77835-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="77835-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="77835-110">Contiene las listas de escalado para el proceso de escalado de 8 x 4, que corresponde a ScalingList \[ 1 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="77835-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="77835-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="77835-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="77835-112">Contiene las listas de escalado para el proceso de escalado de 8 x 4, que corresponde a ScalingList \[ 2 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="77835-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="77835-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="77835-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="77835-114">Contiene las listas de escalado para el proceso de escalado de 8 x 3, que corresponde a ScalingList \[ 3 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 1, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="77835-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="77835-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="77835-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="77835-116">Contiene el valor DC de la lista de escalado para el tamaño 16x16 con sizeID igual a 2 y correspondiente a la \_ lista de escalado \_ DC \_ Coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID igual a 2 y matrixID en el intervalo de 0 a 5, ambos inclusive, en la especificación HEVC.</span><span class="sxs-lookup"><span data-stu-id="77835-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="77835-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="77835-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="77835-118">Contiene el valor DC de la lista de escalado para el tamaño 32x32 con sizeID igual a 3 y correspondiente a la \_ lista de escalado \_ DC \_ Coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID igual a 3 y matrixID en el intervalo de 0 a 1, ambos incluidos, en la especificación HEVC.</span><span class="sxs-lookup"><span data-stu-id="77835-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77835-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77835-119">Requirements</span></span>



| <span data-ttu-id="77835-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77835-120">Requirement</span></span> | <span data-ttu-id="77835-121">Value</span><span class="sxs-lookup"><span data-stu-id="77835-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="77835-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77835-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77835-123">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="77835-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="77835-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77835-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77835-125">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="77835-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="77835-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77835-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77835-127"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="77835-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77835-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="77835-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77835-129">Media Foundation estructuras</span><span class="sxs-lookup"><span data-stu-id="77835-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




