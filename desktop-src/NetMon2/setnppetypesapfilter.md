---
description: Establece el filtro del BLOB ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Función SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360591"
---
# <a name="setnppetypesapfilter-function"></a>SetNPPEtypeSapFilter función)

La función **SetNPPEtypeSapFilter** establece el filtro del BLOB ETYPE/SAP.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*nSaps* \[ de\]
</dt> <dd>

Número de SAP.

</dd> <dt>

*nEtypes* \[ de\]
</dt> <dd>

El número de ETYPE en la tabla ETYPE que se va a establecer.

</dd> <dt>

*lpSapTable* \[ de\]
</dt> <dd>

Un puntero a la tabla de SAP que se establece.

</dd> <dt>

*lpEtypeTable* \[ de\]
</dt> <dd>

Puntero a la tabla ETYPE que se establece.

</dd> <dt>

*FilterFlags* \[ de\]
</dt> <dd>

Marcas de filtro que se establecen.

</dd> <dt>

*hErrorBlob* \[ enuncia\]
</dt> <dd>

Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.

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

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




