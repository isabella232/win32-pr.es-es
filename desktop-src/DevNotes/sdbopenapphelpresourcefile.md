---
description: Carga el archivo de recursos apphelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Función SdbOpenApphelpResourceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044995"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Función SdbOpenApphelpResourceFile

Carga el archivo de recursos apphelp.

## <a name="syntax"></a>Sintaxis


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszACResourceFile* \[ in, opcional\]
</dt> <dd>

Ruta de acceso al archivo de recursos. Si este parámetro es **NULL,** se abre el archivo DLL del recurso local.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un identificador al archivo de recursos abierto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




