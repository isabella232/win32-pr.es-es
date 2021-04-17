---
description: Vuelve a cargar la configuración de color del registro.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660545"
---
# <a name="frefreshstyle-function"></a>FRefreshStyle función)

Vuelve a cargar la configuración de color del registro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve TRUE si se ejecuta correctamente; en caso contrario, FALSE.

## <a name="remarks"></a>Observaciones

Esta función no está asociada a una biblioteca de importación o un archivo de encabezado; se debe llamar mediante las funciones [**LoadLibrary**](-loadlibrary.md) y [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




