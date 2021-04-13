---
title: OP_BLOB
description: Definición de OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "104421570"
---
# <a name="op_blob-structure"></a>Estructura de OP_BLOB

Contiene un búfer de bytes opaco.

## <a name="syntax"></a>Sintaxis

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Miembros

### <a name="cbblob"></a>cbBlob

Especifica el tamaño de pBlob en bytes.

### <a name="pblob"></a>pBlob

Apunta a un búfer de bytes.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)
