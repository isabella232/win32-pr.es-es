---
description: Crea un subárbol del Registro sin conexión que contiene una única clave raíz vacía.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Función ORCreateHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7eae388675cebe300a3dd84607d6bff56078a14addb29d42d6fe76d2b2f6427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045324"
---
# <a name="orcreatehive-function"></a>Función ORCreateHive

Crea un subárbol del Registro sin conexión que contiene una única clave raíz vacía.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phkResult* \[ out\]
</dt> <dd>

Apunta a una variable para recibir un identificador a la clave raíz del subárbol del Registro sin conexión recién creado. Si no se puede crear el subárbol, la función establece este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si no hay memoria suficiente para crear el subárbol del Registro, la función devuelve ERROR \_ NOT \_ ENOUGH \_ MEMORY.

## <a name="remarks"></a>Comentarios

La **función ORCreateHive** crea un subárbol del Registro sin conexión vacío en memoria. Use las [**funciones ORCreateKey**](orcreatekey.md) [**y ORSetValue**](orsetvalue.md) para agregar claves y establecer sus valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
