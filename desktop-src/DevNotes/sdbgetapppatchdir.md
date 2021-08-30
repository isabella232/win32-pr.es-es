---
description: Recupera el directorio AppPatch del sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Función SdbGetAppPatchDir
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 11a92b981112e9165a89f55e15b91ac61cfa06fe88d89117a2f6ecd764f18090
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103665"
---
# <a name="sdbgetapppatchdir-function"></a>Función SdbGetAppPatchDir

Recupera el directorio AppPatch del sistema.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSDB* \[ en, opcional\]
</dt> <dd>

Identificador de la base de datos shim devuelta por la [**función SdbInitDatabase.**](sdbinitdatabase.md)

</dd> <dt>

*szAppPatchPath* \[ out\]
</dt> <dd>

Ruta de acceso resultante.

</dd> <dt>

*cchSize* \[ En\]
</dt> <dd>

Tamaño del búfer *szAppPatchPath,* en caracteres. Si se produce un error en la función, este parámetro se establece en la cadena vacía ("").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




