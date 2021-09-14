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
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173345"
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

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función varias veces para calcular el hash en flujos de datos largos o flujos de datos discontinuos. Se debe llamar a la función [**\_ SHAFinal**](a-shafinal.md) antes de recuperar el valor hash.

Esta función es muy similar a SHAUpdate, pero se llama directamente desde la biblioteca, en lugar de enrutar a través de la infraestructura de criptografía. Para obtener más información, [vea Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
