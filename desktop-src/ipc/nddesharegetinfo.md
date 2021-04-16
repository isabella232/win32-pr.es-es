---
description: Recupera la información del recurso compartido DDE. Esto se suele hacer para editar.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Función NDdeShareGetInfo (Nddeapi. h)
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
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686526"
---
# <a name="nddesharegetinfo-function"></a>NDdeShareGetInfo función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Recupera la información del recurso compartido DDE. Esto se suele hacer para editar.

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

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*lpszShareName* \[ de\]
</dt> <dd>

Nombre del recurso compartido cuya información se va a recuperar del DSDM. Este parámetro no debe ser **null**.

</dd> <dt>

*nLevel* \[ de\]
</dt> <dd>

Nivel de información. Este parámetro debe ser 2.

</dd> <dt>

*lpBuffer* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) y los datos asociados a los que apuntan sus miembros. Este parámetro puede ser **NULL**. Si *lpBuffer* es **null**, el DSDM calcula el número de bytes necesarios para almacenar la información de recurso compartido solicitada y devuelve ese valor en el campo *lpnTotalAvailable* junto con el \_ error de NDDE BUF \_ demasiado \_ pequeño.

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *lpBuffer* , en bytes. Si *lpBuffer* es **null**, *cBufSize* debe ser cero.

</dd> <dt>

*lpnTotalAvailable* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número total de bytes necesarios para almacenar la información de recurso compartido solicitada. Este parámetro no puede ser **null**.

</dd> <dt>

*lpnItems* \[ de\]
</dt> <dd>

Un puntero a una máscara de selección de elementos para la recuperación parcial de información de recursos compartidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el parámetro *lpBuffer* es **null**, devuelve NDDE \_ BUF \_ demasiado \_ pequeño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) y **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




