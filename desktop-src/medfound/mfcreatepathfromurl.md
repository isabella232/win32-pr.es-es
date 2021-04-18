---
description: Convierte una dirección URL de archivo en una ruta de acceso de Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL función)
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
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715369"
---
# <a name="mfcreatepathfromurl-function"></a>MFCreatePathFromURL función)

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones deben llamar a [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]

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

Una cadena terminada en null que contiene la dirección URL. La longitud máxima de la cadena es **longitud máxima de \_ \_ dirección URL \_ de Internet**.

</dd> <dt>

*ppwszFilePath* \[ enuncia\]
</dt> <dd>

Recibe una cadena terminada en null que contiene la dirección URL. El autor de la llamada debe liberar la cadena mediante una llamada a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                                  | Descripción                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ha realizado correctamente. <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido. La cadena especificada en el parámetro *pwszFileURL* no se puede convertir en una ruta de acceso.<br/> |



 

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

 

 
