---
description: Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW función)
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
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540555"
---
# <a name="charupperbuffwrapw-function"></a>CharUpperBuffWrapW función)

\[**CharUpperBuffWrapW** está disponible para su uso en Windows XP. Puede que no esté disponible en versiones posteriores. Debe usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) en su lugar.\]

Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas. La función convierte los caracteres en su lugar.

> [!Note]  
> **CharUpperBuffWrapW** es un contenedor para la función **CharUpperBuffW** . Vea la página [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) para obtener más notas de uso.

 

## <a name="syntax"></a>Sintaxis


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PCH* \[ de\]
</dt> <dd>

Tipo: **LPWStr**

Puntero a un búfer que contiene uno o más caracteres Unicode que se van a procesar.

</dd> <dt>

*cchLength* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Especifica el tamaño, en caracteres, del búfer al que apunta *PCH*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **DWORD**

Número de caracteres procesados.

## <a name="remarks"></a>Observaciones

El método preferido es usar [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) junto con la capa de Microsoft para Unicode (MSLU).

Se debe llamar a **CharUpperBuffWrapW** directamente desde Shlwapi.dll, mediante el ordinal 44.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
