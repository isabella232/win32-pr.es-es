---
description: Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: Función MFCreatePathFromURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: 5f4a2156bde837ef343aa4ca88a18230050d4af6df07012e46fc518d62d898af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113685"
---
# <a name="mfcreatepathfromurl-function"></a>Función MFCreatePathFromURL

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones [**deben llamar a PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]

Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszFileURL* \[ en, opcional\]
</dt> <dd>

Cadena terminada en NULL que contiene la dirección URL. La longitud máxima de la cadena es **INTERNET \_ MAX URL \_ \_ LENGTH**.

</dd> <dt>

*ppwszFilePath* \[ out\]
</dt> <dd>

Recibe una cadena terminada en NULL que contiene la dirección URL. El autor de la llamada debe liberar la cadena llamando [**a CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La función se ha realizado correctamente. <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido. La cadena especificada en el *parámetro pwszFileURL* no se puede convertir en una ruta de acceso.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe usar las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mfplat.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation Functions](media-foundation-functions.md)
</dt> </dl>

 

 
