---
title: Función UtilStringCopyWithAlloc (Ndattributils. h)
description: Asigna y copia una cadena de origen.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676691"
---
# <a name="utilstringcopywithalloc-function"></a>UtilStringCopyWithAlloc función)

La función **UtilStringCopyWithAlloc** asigna y copia una cadena de origen.

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

*Búfer* \[ de enuncia\]
</dt> <dd>

Tipo: **LPWStr \** _

La ubicación donde se almacena el puntero a la memoria asignada. Cuando ya no se necesiten, se debe liberar con [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree). Este búfer siempre termina en NULL.

</dd> <dt>

*BufferMax* \[ de\]
</dt> <dd>

Tipo: **uint**

Número máximo de caracteres que se van a leer del *origen*.

</dd> <dt>

*Origen* \[ de de\]
</dt> <dd>

Tipo: **LPCWSTR**

Cadena que se va a copiar.

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

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

