---
description: El Conectar del objeto Merge conecta un módulo a una característica adicional. El módulo ya se debe haber combinado en la base de datos o se debe combinar en la base de datos. La característica debe existir antes de llamar a esta función.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Combinar. Conectar método (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926675"
---
# <a name="mergeconnect-method"></a>Combinar. Conectar método

El **Conectar** del objeto [**Merge**](merge-object.md) conecta un módulo a una característica adicional. El módulo ya se debe haber combinado en la base de datos o se debe combinar en la base de datos. La característica debe existir antes de llamar a esta función.

Los cambios realizados en la base de datos no se guardan en el disco a menos que se llame al método [**CloseDatabase**](merge-closedatabase.md) con *bCommit* establecido en **TRUE.**

## <a name="syntax"></a>Sintaxis


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Característica* 
</dt> <dd>

Nombre de una característica que ya existe en la base de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Los errores se pueden recuperar a través de [**la propiedad Errors.**](merge-errors.md) Los errores y los mensajes informativos se publican en el archivo de registro actual.

### <a name="c"></a>C++

Consulte [**Conectar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
