---
title: Función CopyHelperAttribute (Ndattributils. h)
description: Crea una copia de una estructura de \_ atributo auxiliar.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676695"
---
# <a name="copyhelperattribute-function"></a>CopyHelperAttribute función)

La función **CopyHelperAttribute** crea una copia de una estructura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dest* \[ enuncia\]
</dt> <dd>

Tipo: **\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _

Estructura que se va a actualizar.

</dd> <dt>

_Source * \[ en\]
</dt> <dd>

Tipo: **\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)const* _

La estructura existente que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                   | Descripción                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se realizó correctamente.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | No se ha proporcionado correctamente uno o más parámetros.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para completar esta operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**atributo auxiliar \_**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





