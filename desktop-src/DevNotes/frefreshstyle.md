---
description: Vuelve a cargar la configuración de color del Registro.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Función FRefreshStyle
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
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103695"
---
# <a name="frefreshstyle-function"></a>Función FRefreshStyle

Vuelve a cargar la configuración de color del Registro.

## <a name="syntax"></a>Sintaxis


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve TRUE si se ejecuta correctamente; de lo contrario, FALSE.

## <a name="remarks"></a>Comentarios

Esta función no está asociada a un archivo de encabezado o biblioteca de importación; Se debe llamar a mediante las [**funciones LoadLibrary**](-loadlibrary.md) [**y GetProcAddress.**](-getprocaddress-.md)

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

 

 




