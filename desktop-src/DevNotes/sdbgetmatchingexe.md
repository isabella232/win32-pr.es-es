---
description: Busca el archivo ejecutable especificado.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907191"
---
# <a name="sdbgetmatchingexe-function"></a>SdbGetMatchingExe función)

Busca el archivo ejecutable especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSDB* \[ en, opcional\]
</dt> <dd>

Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szPath* \[ de\]
</dt> <dd>

Ruta de acceso del archivo ejecutable.

</dd> <dt>

*szModuleName* \[ en, opcional\]
</dt> <dd>

Nombre del módulo.

</dd> <dt>

*pszEnvironment* \[ en, opcional\]
</dt> <dd>

Variables de entorno que se van a usar como contexto de búsqueda.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Este parámetro puede ser 0 o **SDBGMEF \_ omitir \_ entorno** (0x1).

</dd> <dt>

*pQueryResult* \[ enuncia\]
</dt> <dd>

Estructura [**SDBQUERYRESULT**](sdbqueryresult.md) . Si no se encuentra ninguna coincidencia, la estructura contiene **TAGREF \_ null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.

## <a name="remarks"></a>Observaciones

Cuando haya terminado con el [**TAGREF**](tagref.md)devuelto, libere el uso de la función [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




