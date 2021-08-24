---
title: Función UtilStringCopyWithAlloc (Ndattributils.h)
description: Asigna y copia una cadena de origen.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- Función NDF UtilStringCopyWithAlloc
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
ms.openlocfilehash: 3654fa5eefd45a51d963325e10fbcba765420afe25a5c47a058bbaf4e4093ef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801535"
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

Ubicación donde se almacena el puntero a la memoria asignada. Cuando ya no los necesite, debe publicarse [**con CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) Este búfer siempre termina en NULL.

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
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios parámetros no se han proporcionado correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

