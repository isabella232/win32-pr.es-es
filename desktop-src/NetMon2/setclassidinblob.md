---
description: La función SetClassIDInBlob establece el valor de identificador de clase con nombre de un BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Función SetClassIDInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677637"
---
# <a name="setclassidinblob-function"></a>SetClassIDInBlob función)

La función **SetClassIDInBlob** establece el valor de identificador de clase con nombre de un BLOB.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hBlob* \[ de\]
</dt> <dd>

Identificador de un BLOB.

</dd> <dt>

*pOwnerName* \[ de\]
</dt> <dd>

Puntero al nombre del **propietario** del BLOB que se establece.

</dd> <dt>

*pCategoryName* \[ de\]
</dt> <dd>

Puntero al nombre de la **categoría** de BLOB que se establece.

</dd> <dt>

*pTagName* \[ de\]
</dt> <dd>

Puntero al nombre de la **etiqueta** de BLOB que se establece.

</dd> <dt>

*pClsID* \[ de\]
</dt> <dd>

Puntero al identificador de clase del BLOB que se establece.

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

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




