---
description: Convierte una ruta de acceso MS-DOS de Microsoft en una dirección URL canónica.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Función MFCreateURLFromPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739253"
---
# <a name="mfcreateurlfrompath-function"></a>Función MFCreateURLFromPath

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones deben [llamar a UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Convierte una ruta de acceso MS-DOS de Microsoft en una dirección URL canónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszFilePath* \[ in, opcional\]
</dt> <dd>

Cadena terminada en NULL que contiene la ruta de acceso. La longitud máxima de la cadena es **INTERNET \_ MAX URL \_ \_ LENGTH**.

</dd> <dt>

*ppwszFileURL* \[ out\]
</dt> <dd>

Recibe una cadena terminada en NULL que contiene la dirección URL. El autor de la llamada debe liberar la cadena llamando [**a CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un **valor HRESULT.** Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La cadena especificada en el *parámetro pwszFilePath* ya está en formato de dirección URL. En este caso, *pszFilePath simplemente* se copia en *ppszFileURL sin* modificaciones.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | La función se ha realizado correctamente. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

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

 

 
