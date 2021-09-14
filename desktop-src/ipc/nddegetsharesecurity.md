---
description: Recupera el descriptor de seguridad asociado al recurso compartido de DDE. Esto se hace normalmente para su edición.
ms.assetid: 7d3cc965-45ee-40ce-a462-568200592345
title: Función NDdeGetShareSecurity (Nddeapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172293"
---
# <a name="nddegetsharesecurity-function"></a>Función NDdeGetShareSecurity

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera el descriptor de seguridad asociado al recurso compartido de DDE. Esto se hace normalmente para su edición.

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

*lpszServer* \[ En\]
</dt> <dd>

Nombre del servidor en el que reside el DSDM.

</dd> <dt>

*lpszShareName* \[ En\]
</dt> <dd>

Nombre del recurso compartido cuyo descriptor de seguridad se va a recuperar de DSDM. Este parámetro no puede ser **NULL.**

</dd> <dt>

*si* \[ En\]
</dt> <dd>

Valor [**DE \_ INFORMACIÓN DE**](/windows/desktop/SecAuthZ/security-information) SEGURIDAD que especifica la información de seguridad que se va a recuperar del descriptor de seguridad asociado al recurso compartido.

</dd> <dt>

*pSD* \[ out\]
</dt> <dd>

Puntero a una estructura [**\_ DE DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que recibe el descriptor de seguridad auto-relativo. Este parámetro puede ser **NULL**. Si este parámetro es **NULL,** DSDM determina el tamaño de la información de seguridad solicitada y devuelve el número de bytes necesarios en el parámetro *lpcbsdRequired* junto con el código de error TOO SMALL de NDDE \_ \_ BUF. \_

</dd> <dt>

*cbSD* \[ En\]
</dt> <dd>

Tamaño del búfer *pSD.* Este parámetro debe ser cero si *pSD* es **NULL.**

</dd> <dt>

*lpcbsdRequired* \[ out\]
</dt> <dd>

Puntero a la variable que recibe el tamaño real del descriptor de seguridad recuperado. Este parámetro no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NDDE \_ NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es un código de error, que se puede traducir en un mensaje de error de texto llamando a [**NDdeGetErrorString**](nddegeterrorstring.md). Si el *parámetro pSD* era **NULL,** devuelve NDDE \_ BUF \_ TOO \_ SMALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **NDdeGetShareSecurityW** (Unicode) y **NDdeGetShareSecurityA** (ANSI)<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre datos dinámicos Exchange red](network-dynamic-data-exchange.md)
</dt> <dt>

[Funciones DDE de red](network-dde-functions.md)
</dt> <dt>

[**INFORMACIÓN DE \_ SEGURIDAD**](/windows/desktop/SecAuthZ/security-information)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> </dl>

 

