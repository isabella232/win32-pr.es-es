---
title: Función MpManagerVersionQuery (MpClient.h)
description: Devuelve información de versión sobre varios componentes del administrador de protección contra malware.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Características heredadas del entorno de Windows mpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258023"
---
# <a name="mpmanagerversionquery-function"></a>Función MpManagerVersionQuery

Devuelve información de versión sobre varios componentes del administrador de protección contra malware.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*pVersionInfo* \[ out\]
</dt> <dd>

Tipo: **PMPVERSION \_ INFO**

Puntero a una estructura que contiene información de versión sobre varios componentes del administrador de protección contra malware. Vea [**MPVERSION \_ INFO**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores. El autor de la llamada puede [**usar la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**INFORMACIÓN DE \_ MPVERSION**](mpversion-info.md)
</dt> </dl>

 

 





