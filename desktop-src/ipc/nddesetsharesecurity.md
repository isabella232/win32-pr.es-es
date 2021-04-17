---
description: Establece el descriptor de seguridad asociado al recurso compartido DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Función NDdeSetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetShareSecurity
- NDdeSetShareSecurityA
- NDdeSetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 112752bcd0953fbbc358c75080cb2749273ed95d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687974"
---
# <a name="nddesetsharesecurity-function"></a>NDdeSetShareSecurity función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Establece el descriptor de seguridad asociado al recurso compartido DDE. Esto se hace normalmente después de editar la DACL asignada al recurso compartido DDE.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeSetShareSecurity(
  _In_ LPTSTR               lpszServer,
  _In_ LPTSTR               lpszShareName,
  _In_ SECURITY_INFORMATION si,
  _In_ PSECURITY_DESCRIPTOR pSD
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

Nombre del recurso compartido cuyo descriptor de seguridad se va a modificar. Este parámetro no puede ser **null**.

</dd> <dt>

*si* \[ de\]
</dt> <dd>

Valor [**de \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information) que identifica la información de seguridad que se va a recuperar.

</dd> <dt>

*pSD* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de seguridad. Este parámetro no puede ser **null** y debe apuntar a un descriptor de seguridad válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

Para modificar el [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) asociado a un recurso compartido DDE en DSDM, el usuario debe tener el privilegio adecuado. el creador del recurso compartido tiene este privilegio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) y **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**información de seguridad \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

