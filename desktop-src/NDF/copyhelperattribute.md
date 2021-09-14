---
title: Función CopyHelperAttribute (Ndattributils.h)
description: Crea una copia de una estructura HELPER \_ ATTRIBUTE.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- Función CopyHelperAttribute NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161219"
---
# <a name="copyhelperattribute-function"></a>Función CopyHelperAttribute

La **función CopyHelperAttribute** crea una copia de una [**estructura HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **[ **ATRIBUTO \_ DEL ASISTENTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\***

Estructura que se va a actualizar.

</dd> <dt>

*Origen* \[ En\]
</dt> <dd>

Tipo: **atributo auxiliar const [**\_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \***

Estructura existente que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                   | Descripción                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se realizó correctamente.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | No se han proporcionado correctamente uno o varios parámetros.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para completar esta operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ATRIBUTO \_ DEL ASISTENTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





