---
description: La función GetNPPEtypeSapFilter recupera el filtro ETYPE/SAP de un BLOB determinado.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Función GetNPPEtypeSapFilter (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678582"
---
# <a name="getnppetypesapfilter-function"></a>GetNPPEtypeSapFilter función)

La función **GetNPPEtypeSapFilter** recupera el filtro ETYPE/SAP de un BLOB determinado.

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

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*pnSaps* \[ enuncia\]
</dt> <dd>

Puntero al número de protocolos devuelto en la tabla de SAP.

</dd> <dt>

*pnEtypes* \[ enuncia\]
</dt> <dd>

Puntero al número de ETYPE devuelto en la tabla ETYPE.

</dd> <dt>

*ppSapTable* \[ enuncia\]
</dt> <dd>

Puntero a la tabla de SAP devuelta.

</dd> <dt>

*ppEtypeTable* \[ enuncia\]
</dt> <dd>

Puntero a la tabla ETYPE devuelta.

</dd> <dt>

*pFilterFlags* \[ enuncia\]
</dt> <dd>

Puntero a las marcas de filtro devueltas.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error, que especifica la ubicación en el BLOB original donde se produjo el error (si existe).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.

## <a name="remarks"></a>Observaciones

La información de ETYPE/SAP se almacena en la categoría **configuración** de la sección de **propietario** NPP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




