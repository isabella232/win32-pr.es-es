---
description: Vuelve a cargar una configuración de IME desde el registro HKCU, solo en IME japonés.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571625"
---
# <a name="reload_config-function"></a>función reload \_ config

Vuelve a cargar una configuración de IME desde el registro HKCU, solo en IME japonés.

## <a name="syntax"></a>Sintaxis


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Si no hay ningún valor del Registro en HKCU, la función **de \_ configuración reload** escribe los datos iniciales en el registro.

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
