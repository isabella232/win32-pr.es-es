---
description: Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).
ms.assetid: c9814919-412e-4f13-98cc-373b69545734
title: Función NDdeShareAdd (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareAdd
- NDdeShareAddA
- NDdeShareAddW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 282ff7ed3e1564044591966fb4233b2eda1d3227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688304"
---
# <a name="nddeshareadd-function"></a>NDdeShareAdd función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Crea y agrega un nuevo recurso compartido DDE al administrador de bases de datos de recursos compartidos DDE (DSDM).

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeShareAdd(
  _In_ LPTSTR               lpszServer,
  _In_ UINT                 nLevel,
  _In_ PSECURITY_DESCRIPTOR pSD,
  _In_ LPBYTE               lpBuffer,
  _In_ DWORD                cBufSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpszServer* \[ de\]
</dt> <dd>

Nombre del servidor cuyo DSDM se va a modificar.

</dd> <dt>

*nLevel* \[ de\]
</dt> <dd>

Nivel de información. Este parámetro debe ser 2.

</dd> <dt>

*pSD* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que se va a asociar a este recurso compartido y en la que se realizarán las comprobaciones de acceso en los inicios posteriores a este recurso compartido. Este parámetro puede ser **null**, en cuyo caso el DSDM crea un descriptor de seguridad predeterminado que concede "control total" al propietario y "lectura y vinculación" a todos los usuarios.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntero a la estructura [**NDDESHAREINFO**](nddeshareinfo-str.md) que define la lista ApplicationTopic asociada al recurso compartido DDE que se está creando, así como otros parámetros. Este parámetro no puede ser **null**.

</dd> <dt>

*cBufSize* \[ de\]
</dt> <dd>

Tamaño de la estructura *lpBuffer* , en bytes. Este parámetro no puede ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

Para que un cliente pueda conectarse al recurso compartido DDE, debe ser de confianza con [**NDdeSetTrustedShare**](nddesettrustedshare.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeShareAddW** (Unicode) y **NDdeShareAddA** (ANSI)<br/>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

