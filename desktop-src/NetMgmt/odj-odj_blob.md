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
# <a name="odj_blob-structure"></a>Estructura de ODJ_BLOB

Especifica una estructura que contiene una estructura de ODJ_WIN7BLOB serializada o una estructura de OP_PACKAGE serializada.

## <a name="syntax"></a>Sintaxis

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Miembros

### <a name="ulodjformat"></a>ulODJFormat

Especifica la versión lógica de la estructura y debe establecerse en uno de los valores siguientes:

|Value|Significado|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Los bytes contenidos en pBlob deben contener una estructura de ODJ_WIN7_BLOB serializada.|
|ODJ_WIN8_FORMAT (0x00000002)|Los bytes contenidos en pBlob deben contener una estructura de OP_PACKAGE serializada.|

### <a name="cbblob"></a>cbBlob

Debe establecerse en el número de bytes de la matriz pBlob.

### <a name="pblob"></a>pBlob

Apunta a un búfer de bytes que contiene una estructura serializada tal y como se especifica en ulODJFormat anterior.

## <a name="see-also"></a>Vea también

[**Definiciones IDL de unión a dominio sin conexión**](odj-idl.md)

