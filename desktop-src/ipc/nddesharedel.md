---
description: Elimina un recurso compartido DDE del administrador de bases de datos de recursos compartidos DDE (DSDM).
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: Función NDdeShareDel (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686527"
---
# <a name="nddesharedel-function"></a>NDdeShareDel función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Elimina un recurso compartido DDE del administrador de bases de datos de recursos compartidos DDE (DSDM).

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
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

Nombre del recurso compartido que se va a eliminar del DSDM. Este parámetro no puede ser **null**.

</dd> <dt>

*wReserved* \[ de\]
</dt> <dd>

Reservado. Este parámetro debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

Para eliminar un recurso compartido DDE de DSDM, debe tener el privilegio adecuado. El creador del recurso compartido tiene privilegios de eliminación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareDelW** (Unicode) y **NDdeShareDelA** (ANSI)<br/>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> </dl>

 

 




