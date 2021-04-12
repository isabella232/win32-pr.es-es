---
description: Recupera el directorio AppPatch del sistema.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir función)
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
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152707"
---
# <a name="sdbgetapppatchdir-function"></a>SdbGetAppPatchDir función)

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

Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szAppPatchPath* \[ enuncia\]
</dt> <dd>

La ruta de acceso resultante.

</dd> <dt>

*cchSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *szAppPatchPath* , en caracteres. Si se produce un error en la función, este parámetro se establece en la cadena vacía ("").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




