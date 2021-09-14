---
description: Puntero a una función a la que se llama desde el punto de entrada dll.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Puntero de función LPFNInitRoutine (Combase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063193"
---
# <a name="lpfninitroutine-function-pointer"></a>Puntero de función LPFNInitRoutine

Puntero a una función a la que se llama desde el punto de entrada dll.

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

**TRUE** cuando se carga el archivo DLL, **FALSE** cuando se descarga el archivo DLL.

</dd> <dt>

*rclsid* 
</dt> <dd>

Puntero al CLISD del objeto, especificado en la variable miembro [**CFactoryTemplate::m \_ ClsID.**](cfactorytemplate-m-clsid.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este puntero de función no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CFactoryTemplate (clase)**](cfactorytemplate.md)
</dt> </dl>

 

 




