---
title: QueryLayoutOrTipString función)
description: Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o de la lista de perfiles de servicios de texto.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- QueryLayoutOrTipString función de servicios de texto
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686136"
---
# <a name="querylayoutortipstring-function"></a>QueryLayoutOrTipString función)

Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o de la lista de perfiles de servicios de texto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PSZ* \[ de\]
</dt> <dd>

Una cadena que representa una lista de distribución de teclado o una lista de perfiles de servicios de texto.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Todos los diseños o perfiles definidos en *PSZ* son válidos.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno o varios de los diseños o perfiles definidos en *PSZ* no son válidos.<br/> |



 

## <a name="remarks"></a>Observaciones

No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta. Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.

 

El formato de cadena de la lista de diseño es:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

El formato de cadena de la lista de perfiles de servicio de texto es:

<LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};

El siguiente es un ejemplo de un valor para el parámetro *PSZ* :

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

