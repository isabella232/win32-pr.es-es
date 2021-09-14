---
title: Función UtilStringCopyWithAlloc (Ndattributils.h)
description: Asigna y copia una cadena de origen.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Función UtilStringCopyWithAlloc NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071627"
---
# <a name="utilstringcopywithalloc-function"></a>Función UtilStringCopyWithAlloc

La **función UtilStringCopyWithAlloc** asigna y copia una cadena de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Búfer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

Ubicación donde se almacena el puntero a la memoria asignada. Cuando ya no lo necesite, debe publicarse con [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) Este búfer siempre termina en null.

</dd> <dt>

*BufferMax* \[ En\]
</dt> <dd>

Tipo: **UINT**

Número máximo de caracteres que se leerán del *origen*.

</dd> <dt>

*Origen* \[ En\]
</dt> <dd>

Tipo: **LPCWSTR**

Cadena que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                  | Descripción                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se han proporcionado correctamente uno o varios parámetros.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

