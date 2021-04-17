---
description: Establece la información de recursos compartidos DDE. Normalmente, esto se realiza después de la edición.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Función NDdeShareSetInfo (Nddeapi. h)
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
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686525"
---
# <a name="nddesharesetinfo-function"></a>NDdeShareSetInfo función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Establece la información de recursos compartidos DDE. Normalmente, esto se realiza después de la edición.

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

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor cuyo DSDM se va a modificar.

</dd> <dt>

*lpszShareName* \[ de\]
</dt> <dd>

Nombre del nombre del recurso compartido cuya información se va a modificar. Este parámetro no puede ser **null**.

</dd> <dt>

*nLevel* \[ de\]
</dt> <dd>

Nivel de información. Este parámetro debe ser 2.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntero a la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) que especifica la información de recursos compartidos DDE que se va a almacenar en el DSDM. Actualmente, la información de los recursos compartidos DDE se modifica en su totalidad, es decir, no se realiza ninguna edición parcial. Este parámetro no puede ser **null**.

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño del búfer de *lpBuffer* , en bytes.

</dd> <dt>

*sParmNum* \[ de\]
</dt> <dd>

Índice del parámetro que se va a modificar. La implementación actual no admite la modificación parcial; por lo tanto, este parámetro debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) y **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




