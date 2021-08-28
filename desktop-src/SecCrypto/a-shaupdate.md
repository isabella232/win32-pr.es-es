---
description: Agrega datos a un objeto hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate función (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 103438e3ef0747aa6170848398621b0246bd15366be4d1171ce5735942011007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101075"
---
# <a name="a_shaupdate-function"></a>Una \_ función SHAUpdate

Agrega datos a un objeto hash especificado.

## <a name="syntax"></a>Sintaxis


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contexto* \[ in, out\]
</dt> <dd>

Contexto SHA.

</dd> <dt>

*Búfer* \[ out\]
</dt> <dd>

Tabla hash.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Tamaño del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función varias veces para calcular el hash en flujos de datos largos o flujos de datos discontinuos. Se debe llamar a la función [**\_ SHAFinal**](a-shafinal.md) antes de recuperar el valor hash.

Esta función es muy similar a SHAUpdate, pero se llama directamente desde la biblioteca, en lugar de enrutar a través de la infraestructura de criptografía. Para obtener más información, [vea Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
