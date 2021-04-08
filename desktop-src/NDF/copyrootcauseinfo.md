---
title: Función CopyRootCauseInfo (Ndattributils. h)
description: Crea una copia de una estructura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo función NDF
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996174"
---
# <a name="copyrootcauseinfo-function"></a>CopyRootCauseInfo función)

La función **CopyRootCauseInfo** crea una copia de una estructura [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dest* \[ enuncia\]
</dt> <dd>

Tipo: **[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Estructura que se va a actualizar.

</dd> <dt>

_Source * \[ en\]
</dt> <dd>

Tipo: **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





