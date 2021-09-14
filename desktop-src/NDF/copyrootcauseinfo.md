---
title: Función CopyRootCauseInfo (Ndattributils.h)
description: Crea una copia de una estructura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Función CopyRootCauseInfo NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161216"
---
# <a name="copyrootcauseinfo-function"></a>Función CopyRootCauseInfo

La **función CopyRootCauseInfo** crea una copia de una [**estructura RootCauseInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Tipo: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Estructura que se va a actualizar.

</dd> <dt>

*Origen* \[ En\]
</dt> <dd>

Tipo: **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \***

Estructura existente que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Los valores devueltos posibles incluyen, entre otros, lo siguiente.



| Código devuelto                                                                                   | Descripción                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se realizó correctamente.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno o varios parámetros no se han proporcionado correctamente.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria disponible para completar esta operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





