---
description: Puntero a una función a la que se llama desde el punto de entrada de DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntero a la función LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679470"
---
# <a name="lpfninitroutine-function-pointer"></a>Puntero a la función LPFNInitRoutine

Puntero a una función a la que se llama desde el punto de entrada de DLL.

## <a name="syntax"></a>Sintaxis


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bLoading* 
</dt> <dd>

**True** cuando se carga el archivo dll, **false** cuando se descarga el archivo dll.

</dd> <dt>

*rclsid* 
</dt> <dd>

Puntero a la CLISD del objeto, que se especifica en la variable miembro [**CFactoryTemplate:: m \_ ClsID**](cfactorytemplate-m-clsid.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este puntero de función no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




