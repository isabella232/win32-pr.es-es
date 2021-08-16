---
description: Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Función CharUpperBuffWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861560"
---
# <a name="charupperbuffwrapw-function"></a>Función CharUpperBuffWrapW

\[**CharUpperBuffWrapW** está disponible para su uso en Windows XP. Es posible que no esté disponible en versiones posteriores. Debe usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) en su lugar.\]

Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas. La función convierte los caracteres en su lugar.

> [!Note]  
> **CharUpperBuffWrapW es** un contenedor para la **función CharUpperBuffW.** Consulte la [**página CharUpperBuff para**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pch* \[ En\]
</dt> <dd>

Tipo: **LPWSTR**

Puntero a un búfer que contiene uno o varios caracteres Unicode que se procesarán.

</dd> <dt>

*cchLength* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Especifica el tamaño, en caracteres, del búfer al que apunta *pch*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Número de caracteres procesados.

## <a name="remarks"></a>Comentarios

El método preferido es usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **CharUpperBuffWrapW** directamente desde Shlwapi.dll, mediante el ordinal 44.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
