---
description: Recupera la información del recurso compartido de DDE. Normalmente, esto se hace para la edición.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Función NDdeShareGetInfo (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2c622a611b3d917dcf67de2ec6b96070ec0e54e9e53b0cef04c3c9e35b859e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014756"
---
# <a name="nddesharegetinfo-function"></a>Función NDdeShareGetInfo

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera la información del recurso compartido de DDE. Normalmente, esto se hace para la edición.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*lpszShareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido cuya información se va a recuperar del DSDM. Este parámetro no debe ser **NULL.**

</dd> <dt>

*nLevel* \[ En\]
</dt> <dd>

Nivel de información. Este parámetro debe ser 2.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) y los datos asociados a los que apuntan sus miembros. Este parámetro puede ser **NULL**. Si *lpBuffer* es **NULL,** DSDM calcula el número de bytes necesarios para almacenar la información de recurso compartido solicitado y devuelve ese valor en el campo *lpnTotalAvailable* junto con el error NDDE \_ BUF \_ TOO \_ SMALL.

</dd> <dt>

*cBufSize* \[ En\]
</dt> <dd>

Tamaño del búfer *lpBuffer,* en bytes. Si *lpBuffer* es **NULL,** *cBufSize* debe ser cero.

</dd> <dt>

*lpnTotalAvailable* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número total de bytes necesarios para almacenar la información de recurso compartido solicitada. Este parámetro no puede ser **NULL.**

</dd> <dt>

*lpnItems* \[ En\]
</dt> <dd>

Puntero a una máscara de selección de elementos para la recuperación parcial de información de recursos compartidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el *parámetro lpBuffer* **es NULL,** devuelve NDDE \_ BUF TOO \_ \_ SMALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) y **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




