---
title: ODJ_BLOB
description: ODJ_BLOB definición de IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566949"
---
# <a name="odj_blob-structure"></a>ODJ_BLOB estructura

Especifica una estructura que contiene una estructura ODJ_WIN7BLOB serializada o una estructura OP_PACKAGE serializada.

## <a name="syntax"></a>Sintaxis

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Members

### <a name="ulodjformat"></a>ulODJFormat

Especifica la versión lógica de la estructura y debe establecerse en uno de los valores siguientes:

|Value|Significado|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Los bytes contenidos en pBlob deben contener una estructura ODJ_WIN7_BLOB serializada.|
|ODJ_WIN8_FORMAT (0x00000002)|Los bytes contenidos en pBlob deben contener una estructura OP_PACKAGE serializada.|

### <a name="cbblob"></a>cbBlob

Debe establecerse en el número de bytes de la matriz pBlob.

### <a name="pblob"></a>pBlob

Apunta a un búfer de bytes que contiene una estructura serializada tal como se especifica en ulODJFormat anterior.

## <a name="see-also"></a>Vea también

[**Definiciones de IDL de unión a un dominio sin conexión**](odj-idl.md)

