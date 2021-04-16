---
description: Crea un subárbol del registro sin conexión que contiene una única clave raíz vacía.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Función ORCreateHive (Offreg. h)
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
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650096"
---
# <a name="orcreatehive-function"></a>ORCreateHive función)

Crea un subárbol del registro sin conexión que contiene una única clave raíz vacía.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phkResult* \[ enuncia\]
</dt> <dd>

Apunta a una variable para recibir un identificador a la clave raíz del subárbol del registro sin conexión recién creado. Si no se puede crear el subárbol, la función establece este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si no hay memoria suficiente para crear el subárbol del registro, la función devuelve un ERROR que indica que \_ no \_ hay suficiente \_ memoria.

## <a name="remarks"></a>Observaciones

La función **ORCreateHive** crea un subárbol del registro sin conexión vacío en la memoria. Use las funciones [**ORCreateKey**](orcreatekey.md) y [**ORSetValue**](orsetvalue.md) para agregar claves y establecer sus valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 
