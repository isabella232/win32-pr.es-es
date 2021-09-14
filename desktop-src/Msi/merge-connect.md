---
description: El Conectar del objeto Merge conecta un módulo a una característica adicional. El módulo ya se debe haber combinado en la base de datos o se combinará en la base de datos. La característica debe existir antes de llamar a esta función.
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
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074394"
---
# <a name="mergeconnect-method"></a>Combinar. Conectar método

El **Conectar** del objeto [**Merge**](merge-object.md) conecta un módulo a una característica adicional. El módulo ya se debe haber combinado en la base de datos o se combinará en la base de datos. La característica debe existir antes de llamar a esta función.

Los cambios realizados en la base de datos no se guardan en el disco a menos que se llame al [**método CloseDatabase**](merge-closedatabase.md) con *bCommit* establecido en **TRUE.**

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

## <a name="remarks"></a>Observaciones

Los errores se pueden recuperar a través de [**la propiedad Errors.**](merge-errors.md) Los errores y los mensajes informativos se publican en el archivo de registro actual.

### <a name="c"></a>C++

Consulte [**Conectar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
