---
description: Lee una línea de Setup. inf y extrae el campo especificado de la cadena.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Función ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277413"
---
# <a name="parsefield-function"></a>ParseField función)

\[Actualmente se espera que la función **ParseField** esté disponible para su uso en la siguiente versión del sistema operativo Microsoft Windows. Podría modificarse o no estar disponible en versiones posteriores.\]

Lee una línea de Setup. inf y extrae el campo especificado de la cadena.

## <a name="syntax"></a>Sintaxis


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szData* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR \** _

Un puntero a la línea de Setup. inf.

</dd> <dt>

_n * \[ en\]
</dt> <dd>

Tipo: **int**

**Entero** que indica el campo que se va a extraer.

<dt>



  (0)


</dt> <dd>

Indica el campo delante de un signo igual (=).

</dd> <dt>



 (1)


</dt> <dd>

Indica el primer campo.

</dd> </dl> </dd> <dt>

*szBuf* \[ de\]
</dt> <dd>

Tipo: **LPTSTR \** _

Puntero al búfer que recibe el campo extraído.

</dd> <dt>

_iBufLen * \[ en\]
</dt> <dd>

Tipo: **int**

**Int** que recibe el tamaño del búfer que recibe el campo extraído.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve **true** si la función es correcta y **false** si se produce un error.

## <a name="remarks"></a>Observaciones

Los campos de la cadena deben estar separados por comas.

Se quitan los espacios iniciales y finales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Util. h</dt> </dl>                             |
| Biblioteca<br/>                  | <dl> <dt>Shell32. lib</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 




