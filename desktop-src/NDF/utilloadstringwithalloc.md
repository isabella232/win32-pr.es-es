---
title: Función UtilLoadStringWithAlloc (Ndattributils.h)
description: Asigna y carga una cadena fuera de la tabla de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- Función UtilLoadStringWithAlloc NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071626"
---
# <a name="utilloadstringwithalloc-function"></a>Función UtilLoadStringWithAlloc

La **función UtilLoadStringWithAlloc** asigna y carga una cadena fuera de la tabla de recursos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uID* \[ En\]
</dt> <dd>

Tipo: **UINT**

Identificador de la cadena que se va a cargar.

</dd> <dt>

*ppwzBuffer* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \***

Ubicación donde se colocará la cadena recién asignada. La cadena debe liberarse mediante [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no sea necesaria.

</dd> <dt>

*cchBufferMax* \[ En\]
</dt> <dd>

Tipo: **UINT**

Número máximo de caracteres que se cargarán desde la tabla de recursos. Si la cadena de recurso es mayor que el número de caracteres especificado, se trunca y finaliza en NULL.

> [!Note]  
> Este parámetro no se puede establecer en cero.

 

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

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

