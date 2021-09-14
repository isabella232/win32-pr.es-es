---
description: La función GetNPPEtypeSapFilter recupera el filtro Etype/Sap de un BLOB determinado.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Función GetNPPEtypeSapFilter (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171457"
---
# <a name="getnppetypesapfilter-function"></a>Función GetNPPEtypeSapFilter

La **función GetNPPEtypeSapFilter** recupera el filtro Etype/Sap de un BLOB determinado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*pnSaps* \[ out\]
</dt> <dd>

Puntero al número devuelto de protocolos en la tabla de SAP.

</dd> <dt>

*pnEtypes* \[ out\]
</dt> <dd>

Puntero al número devuelto de Etypes en la tabla Etype.

</dd> <dt>

*ppSapTable* \[ out\]
</dt> <dd>

Puntero a la tabla de SAP devuelta.

</dd> <dt>

*ppEtypeTable* \[ out\]
</dt> <dd>

Puntero a la tabla Etype devuelta.

</dd> <dt>

*pFilterFlags* \[ out\]
</dt> <dd>

Puntero a las marcas de filtro devueltas.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Controlar un BLOB de error, que especifica la ubicación en el BLOB original donde se produjo el error (si lo hubiera).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el error.

## <a name="remarks"></a>Observaciones

La información de Etype/Sap se almacena en la **categoría Config** de la sección Propietario **de** NPP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




