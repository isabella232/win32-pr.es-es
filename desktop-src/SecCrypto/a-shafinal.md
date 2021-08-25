---
description: Calcula el hash final de los datos especificados por la función MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: A_SHAFinal (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 42a22cfca32409fdfa02586bb90c76f8e8f2489b22cfe2769b50d928d2564af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960295"
---
# <a name="a_shafinal-function"></a>Una \_ función SHAFinal

Calcula el hash final de los datos especificados por la función MD5Update.

## <a name="syntax"></a>Sintaxis


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Contexto* \[ in, out\]
</dt> <dd>

Contexto SHA.

</dd> <dt>

*Resultado* \[ out\]
</dt> <dd>

Tabla hash resultante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función es muy similar a SHAFinal, pero se llama directamente desde la biblioteca, en lugar de enrutada a través de la infraestructura de criptografía. Para obtener más información, [vea Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
