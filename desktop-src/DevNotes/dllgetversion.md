---
description: La función DllGetVersion recupera el número de versión de Cabinet.dll mediante la estructura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Función DllGetVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 7671465d20987de9ebe526db5961513c81cea5b30d6ad095baf4d3df3d798194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654045"
---
# <a name="dllgetversion-function"></a>Función DllGetVersion

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]

La **función DllGetVersion** recupera el número de versión de Cabinet.dll utilizando la [**estructura CABINETDLLVERSIONINFO.**](cabinetdllversioninfo.md)

## <a name="syntax"></a>Sintaxis


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcdvi* 
</dt> <dd>

Puntero a la [**estructura CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) que contiene la información de versión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
