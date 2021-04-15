---
title: ODJ_BLOB
description: Definición de ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104488482"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="c8ef2-103">Estructura de ODJ_BLOB</span><span class="sxs-lookup"><span data-stu-id="c8ef2-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="c8ef2-104">Especifica una estructura que contiene una estructura de ODJ_WIN7BLOB serializada o una estructura de OP_PACKAGE serializada.</span><span class="sxs-lookup"><span data-stu-id="c8ef2-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ef2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8ef2-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="c8ef2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8ef2-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="c8ef2-107">ulODJFormat</span><span class="sxs-lookup"><span data-stu-id="c8ef2-107">ulODJFormat</span></span>

<span data-ttu-id="c8ef2-108">Especifica la versión lógica de la estructura y debe establecerse en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8ef2-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="c8ef2-109">Value</span><span class="sxs-lookup"><span data-stu-id="c8ef2-109">Value</span></span>|<span data-ttu-id="c8ef2-110">Significado</span><span class="sxs-lookup"><span data-stu-id="c8ef2-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="c8ef2-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c8ef2-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="c8ef2-112">Los bytes contenidos en pBlob deben contener una estructura de ODJ_WIN7_BLOB serializada.</span><span class="sxs-lookup"><span data-stu-id="c8ef2-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="c8ef2-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c8ef2-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="c8ef2-114">Los bytes contenidos en pBlob deben contener una estructura de OP_PACKAGE serializada.</span><span class="sxs-lookup"><span data-stu-id="c8ef2-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="c8ef2-115">cbBlob</span><span class="sxs-lookup"><span data-stu-id="c8ef2-115">cbBlob</span></span>

<span data-ttu-id="c8ef2-116">Debe establecerse en el número de bytes de la matriz pBlob.</span><span class="sxs-lookup"><span data-stu-id="c8ef2-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="c8ef2-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="c8ef2-117">pBlob</span></span>

<span data-ttu-id="c8ef2-118">Apunta a un búfer de bytes que contiene una estructura serializada tal y como se especifica en ulODJFormat anterior.</span><span class="sxs-lookup"><span data-stu-id="c8ef2-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8ef2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ef2-119">See also</span></span>

[<span data-ttu-id="c8ef2-120">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="c8ef2-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

