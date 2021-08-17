---
description: Inicia el hash de un flujo de datos.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: A_SHAInit función (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0081311988a5da0ae5ca21e924305918bb1e713a6cde3be1b77821c9b458cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774270"
---
# <a name="a_shainit-function"></a>Una \_ función SHAInit

Inicia el hash de un flujo de datos.

## <a name="syntax"></a>Sintaxis


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contexto* \[ in, out\]
</dt> <dd>

Contexto SHA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función es muy similar a SHAInit, pero se llama directamente desde la biblioteca, en lugar de enrutada a través de la infraestructura de criptografía. Para obtener más información, [vea Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
