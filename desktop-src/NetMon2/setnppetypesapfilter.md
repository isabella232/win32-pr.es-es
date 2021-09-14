---
description: Establece el filtro BLOB Etype/Sap.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Función SetNPPEtypeSapFilter (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245210"
---
# <a name="setnppetypesapfilter-function"></a>Función SetNPPEtypeSapFilter

La **función SetNPPEtypeSapFilter** establece el filtro BLOB Etype/Sap.

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

*hBlob* \[ En\]
</dt> <dd>

Identificador del BLOB.

</dd> <dt>

*nSaps* \[ En\]
</dt> <dd>

Número de SAP.

</dd> <dt>

*nEtypes* \[ En\]
</dt> <dd>

Número de Etypes de la tabla Etype que se va a establecer.

</dd> <dt>

*lpSapTable* \[ En\]
</dt> <dd>

Puntero a la tabla de SAP que se establece.

</dd> <dt>

*lpEtypeTable* \[ En\]
</dt> <dd>

Puntero a la tabla Etype que se establece.

</dd> <dt>

*FilterFlags* \[ En\]
</dt> <dd>

Marcas de filtro que se establecen.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Identificador de un BLOB de error que especifica dónde se produjo el error (si lo hubiera) en el BLOB original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un valor NMERR que indica el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




