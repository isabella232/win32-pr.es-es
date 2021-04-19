---
title: OP_PACKAGE
description: Definición de OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720188"
---
# <a name="op_package-structure"></a><span data-ttu-id="c717a-103">Estructura de OP_PACKAGE</span><span class="sxs-lookup"><span data-stu-id="c717a-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="c717a-104">Contiene una estructura que contiene un OP_PACKAGE_COLLECTION serializado.</span><span class="sxs-lookup"><span data-stu-id="c717a-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="c717a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c717a-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a><span data-ttu-id="c717a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c717a-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="c717a-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="c717a-107">EncryptionType</span></span>

<span data-ttu-id="c717a-108">Reservado para uso futuro y debe establecerse en GUID_NULL.</span><span class="sxs-lookup"><span data-stu-id="c717a-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="c717a-109">EncryptionContext</span><span class="sxs-lookup"><span data-stu-id="c717a-109">EncryptionContext</span></span>

<span data-ttu-id="c717a-110">Reservado para uso futuro y debe establecerse en ceros.</span><span class="sxs-lookup"><span data-stu-id="c717a-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="c717a-111">WrappedPartCollection</span><span class="sxs-lookup"><span data-stu-id="c717a-111">WrappedPartCollection</span></span>

<span data-ttu-id="c717a-112">OP_BLOB estructura que contiene una estructura de OP_PACKAGE_COLLECTION serializada.</span><span class="sxs-lookup"><span data-stu-id="c717a-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="c717a-113">cbDecryptedPartCollection</span><span class="sxs-lookup"><span data-stu-id="c717a-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="c717a-114">Reservado para uso futuro y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="c717a-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="c717a-115">Extensión</span><span class="sxs-lookup"><span data-stu-id="c717a-115">Extension</span></span>

<span data-ttu-id="c717a-116">Reservado para uso futuro y debe establecerse en ceros.</span><span class="sxs-lookup"><span data-stu-id="c717a-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="c717a-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c717a-117">See also</span></span>

[<span data-ttu-id="c717a-118">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="c717a-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="c717a-119">**BLOB de operaciones \_**</span><span class="sxs-lookup"><span data-stu-id="c717a-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="c717a-120">**\_colección de paquetes de OP \_**</span><span class="sxs-lookup"><span data-stu-id="c717a-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
