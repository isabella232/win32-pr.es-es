---
description: Recupera el nombre para mostrar de la etiqueta especificada.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString función)
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
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496096"
---
# <a name="sdbtagtostring-function"></a>SdbTagToString función)

Recupera el nombre para mostrar de la etiqueta especificada.

## <a name="syntax"></a>Sintaxis


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*etiqueta* \[ de de\]
</dt> <dd>

ETIQUETA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un puntero a la cadena terminada en null o "InvalidTag".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ETIQUETA**](tag.md)
</dt> </dl>

 

 




