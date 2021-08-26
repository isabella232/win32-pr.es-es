---
description: Recupera el nombre para mostrar de la etiqueta especificada.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Función SdbTagToString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044845"
---
# <a name="sdbtagtostring-function"></a>Función SdbTagToString

Recupera el nombre para mostrar de la etiqueta especificada.

## <a name="syntax"></a>Sintaxis


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*etiqueta* \[ En\]
</dt> <dd>

ETIQUETA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un puntero a la cadena terminada en NULL o "InvalidTag".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**etiqueta**](tag.md)
</dt> </dl>

 

 




