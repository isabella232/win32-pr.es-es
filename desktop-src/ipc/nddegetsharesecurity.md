---
description: Recupera el descriptor de seguridad asociado al recurso compartido DDE. Esto se hace normalmente para la edición.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Función NDdeGetShareSecurity (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetShareSecurity
- NDdeGetShareSecurityA
- NDdeGetShareSecurityW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: dae1352d9e7c45f9ce301dd30d4e7f73d508498c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912970"
---
# <a name="nddegetsharesecurity-function"></a>NDdeGetShareSecurity función)

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Recupera el descriptor de seguridad asociado al recurso compartido DDE. Esto se hace normalmente para la edición.

## <a name="syntax"></a>Sintaxis


```C++
UINT NDdeGetShareSecurity(
  _In_  LPTSTR               lpszServer,
  _In_  LPTSTR               lpszShareName,
  _In_  SECURITY_INFORMATION si,
  _Out_ PSECURITY_DESCRIPTOR pSD,
  _In_  DWORD                cbSD,
  _Out_ LPDWORD              lpcbsdRequired
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

Nombre del recurso compartido cuyo descriptor de seguridad se va a recuperar del DSDM. Este parámetro no puede ser **null**.

</dd> <dt>

*si* \[ de\]
</dt> <dd>

Valor [**de \_ información de seguridad**](/windows/desktop/SecAuthZ/security-information) que especifica la información de seguridad que se va a recuperar del descriptor de seguridad asociado al recurso compartido.

</dd> <dt>

*pSD* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que recibe el descriptor de seguridad autorelativo. Este parámetro puede ser **NULL**. Si este parámetro es **null**, el DSDM determina el tamaño de la información de seguridad solicitada y devuelve el número de bytes necesarios en el parámetro *lpcbsdRequired* junto con el código de error de NDDE \_ BUF \_ demasiado \_ pequeño.

</dd> <dt>

*cbSD* \[ de\]
</dt> <dd>

Tamaño del búfer *pSD* . Este parámetro debe ser cero si *pSD* es **null**.

</dd> <dt>

*lpcbsdRequired* \[ enuncia\]
</dt> <dd>

Puntero a la variable que recibe el tamaño real del descriptor de seguridad recuperado. Este parámetro no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es NDDE \_ sin \_ error.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto mediante una llamada a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el parámetro *pSD* era **null**, devolverá NDDE \_ BUF \_ demasiado \_ pequeño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) y **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general de Intercambio dinámico de datos de red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**información de seguridad \_**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

