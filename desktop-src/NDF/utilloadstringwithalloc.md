---
title: Función UtilLoadStringWithAlloc (Ndattributils. h)
description: Asigna y carga una cadena fuera de la tabla de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151226"
---
# <a name="utilloadstringwithalloc-function"></a>UtilLoadStringWithAlloc función)

La función **UtilLoadStringWithAlloc** asigna y carga una cadena fuera de la tabla de recursos.

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

*uID* \[ de\]
</dt> <dd>

Tipo: **uint**

Identificador de de la cadena que se va a cargar.

</dd> <dt>

*ppwzBuffer* \[ enuncia\]
</dt> <dd>

Tipo: **LPWStr \** _

Ubicación donde se colocará la cadena recién asignada. La cadena se debe liberar mediante [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) cuando ya no se necesite.

</dd> <dt>

*cchBufferMax* \[ de\]
</dt> <dd>

Tipo: **uint**

Número máximo de caracteres que se van a cargar desde la tabla de recursos. Si la cadena de recursos es mayor que el número de caracteres especificado, se trunca y termina en NULL.

> [!Note]  
> Este parámetro no se puede establecer en cero.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                  | Descripción                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La operación se realizó correctamente.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No se ha proporcionado correctamente uno o más parámetros.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

