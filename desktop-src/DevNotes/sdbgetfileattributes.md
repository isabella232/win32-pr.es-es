---
description: Recupera los datos de atributo para el archivo especificado.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152704"
---
# <a name="sdbgetfileattributes-function"></a>SdbGetFileAttributes función)

Recupera los datos de atributo para el archivo especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpwszFileName* \[ de\]
</dt> <dd>

Ruta de acceso al archivo.

</dd> <dt>

*ppAttrInfo* \[ enuncia\]
</dt> <dd>

Matriz de estructuras [**ATTRINFO**](attrinfo.md) que contienen los datos del atributo.

</dd> <dt>

*lpdwAttrCount* \[ enuncia\]
</dt> <dd>

Número de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="remarks"></a>Observaciones

Cuando haya terminado con los datos, libere el uso de la función [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




