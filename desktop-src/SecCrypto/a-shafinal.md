---
description: Calcula el hash final de los datos especificados por la función MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Función A_SHAFinal (Sha. h)
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
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670396"
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

*Contexto* \[ de in, out\]
</dt> <dd>

Contexto SHA.

</dd> <dt>

*Resultado* \[ de enuncia\]
</dt> <dd>

Tabla hash resultante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función es muy similar a SHAFinal, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía. Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
