---
description: Establece el descriptor de seguridad asociado al recurso compartido de DDE.
ms.assetid: 8bb8c466-3dd7-49a6-8ba5-632001b8a47f
title: Función NDdeSetShareSecurity (Nddeapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172286"
---
# <a name="nddesetsharesecurity-function"></a>Función NDdeSetShareSecurity

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Establece el descriptor de seguridad asociado al recurso compartido de DDE. Esto se hace normalmente después de editar la DACL asignada al recurso compartido de DDE.

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

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor cuyo DSDM se va a modificar.

</dd> <dt>

*lpszShareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido cuyo descriptor de seguridad se va a modificar. Este parámetro no puede ser **NULL.**

</dd> <dt>

*si* \[ En\]
</dt> <dd>

Valor [**DE \_ INFORMACIÓN DE**](/windows/desktop/SecAuthZ/security-information) SEGURIDAD que identifica la información de seguridad que se debe recuperar.

</dd> <dt>

*pSD* \[ En\]
</dt> <dd>

Puntero a una estructura [**\_ DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de seguridad. Este parámetro no puede ser **NULL** y debe apuntar a un descriptor de seguridad válido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="remarks"></a>Observaciones

Para modificar el [**\_ DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) asociado a un recurso compartido de DDE en DSDM, el usuario debe tener el privilegio adecuado; el creador del recurso compartido tiene este privilegio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeSetShareSecurityW** (Unicode) y **NDdeSetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**INFORMACIÓN DE \_ SEGURIDAD**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeGetShareSecurity**](nddegetsharesecurity.md)
</dt> </dl>

 

