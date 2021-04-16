---
description: Inicia el hash de un flujo de datos.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Función A_SHAInit (Sha. h)
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
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689990"
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

*Contexto* \[ de in, out\]
</dt> <dd>

Contexto SHA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función es muy similar a SHAInit, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía. Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
