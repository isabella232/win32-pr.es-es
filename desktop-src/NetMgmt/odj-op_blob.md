---
title: OP_BLOB
description: OP_BLOB definición de IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566921"
---
# <a name="op_blob-structure"></a>OP_BLOB estructura

Contiene un búfer de bytes opaco.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Members

### <a name="cbblob"></a>cbBlob

Especifica el tamaño de pBlob en bytes.

### <a name="pblob"></a>pBlob

Apunta a un búfer de bytes.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)
