---
description: Agrega datos a un objeto hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Función A_SHAUpdate (Sha. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689989"
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

*Contexto* \[ de in, out\]
</dt> <dd>

Contexto SHA.

</dd> <dt>

*Búfer* \[ de enuncia\]
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

Se puede llamar a esta función varias veces para calcular el hash en flujos de datos largos o en flujos de datos descontinuos. Se debe llamar a la función [**\_ SHAFinal**](a-shafinal.md) antes de recuperar el valor hash.

Esta función es muy similar a SHAUpdate, pero se llama directamente desde la biblioteca, en lugar de enrutarse a través de la infraestructura de criptografía. Para obtener más información, consulte [proveedores de Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
