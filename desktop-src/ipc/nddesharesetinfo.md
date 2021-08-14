---
description: Establece la información del recurso compartido de DDE. Esto suele hacerse después de la edición.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Función NDdeShareSetInfo (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: ccfa8cc80f60477e8512ac43f0e93825642dd0603ee398e232bbb67d6979a4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481705"
---
# <a name="nddesharesetinfo-function"></a>Función NDdeShareSetInfo

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Establece la información del recurso compartido de DDE. Esto suele hacerse después de la edición.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor cuyo DSDM se va a modificar.

</dd> <dt>

*lpszShareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido cuya información se va a modificar. Este parámetro no puede ser **NULL.**

</dd> <dt>

*nLevel* \[ En\]
</dt> <dd>

Nivel de información. Este parámetro debe ser 2.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntero a la [**estructura NDDESHAREINFO**](nddeshareinfo-str.md) que especifica la información del recurso compartido de DDE que se va a almacenar en DSDM. Actualmente, la información del recurso compartido de DDE se modifica en su totalidad, es decir, no se realizan modificaciones parciales. Este parámetro no puede ser **NULL.**

</dd> <dt>

*cBufSize* \[ En\]
</dt> <dd>

Tamaño del búfer *lpBuffer,* en bytes.

</dd> <dt>

*sParmNum* \[ En\]
</dt> <dd>

Índice de parámetros que se va a modificar. La implementación actual no admite la modificación parcial; por lo tanto, este parámetro debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) y **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




