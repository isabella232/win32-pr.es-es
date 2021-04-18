---
description: Convierte una ruta de acceso de Microsoft MS-DOS en una dirección URL con formato canónico.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath función)
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
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715370"
---
# <a name="mfcreateurlfrompath-function"></a>MFCreateURLFromPath función)

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones deben llamar a [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Convierte una ruta de acceso de Microsoft MS-DOS en una dirección URL con formato canónico.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszFilePath* \[ en, opcional\]
</dt> <dd>

Una cadena terminada en null que contiene la ruta de acceso. La longitud máxima de la cadena es **longitud máxima de \_ \_ dirección URL \_ de Internet**.

</dd> <dt>

*ppwszFileURL* \[ enuncia\]
</dt> <dd>

Recibe una cadena terminada en null que contiene la dirección URL. El autor de la llamada debe liberar la cadena mediante una llamada a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La cadena especificada en el parámetro *pwszFilePath* ya está en formato de dirección URL. En este caso, *pszFilePath* simplemente se copia en *ppszFileURL* sin modificarlo.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | La función se ha realizado correctamente. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Esta función no tiene ninguna biblioteca de importación asociada. Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mfplat.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
