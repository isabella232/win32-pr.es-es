---
description: Recupera el título del archivo para la ruta de acceso de archivo especificada.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: Función pSetupGetFileTitle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 2fac93fc43b533ecb60d248e424855229c3f6f5f504ef6b43522c8d44d145799
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386515"
---
# <a name="psetupgetfiletitle-function"></a>Función pSetupGetFileTitle

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Recupera el título del archivo para la ruta de acceso de archivo especificada.

## <a name="syntax"></a>Sintaxis


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FilePath* \[ En\]
</dt> <dd>

Ruta de acceso al archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Puntero a la cadena que recibe el título del archivo.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
