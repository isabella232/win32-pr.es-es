---
description: La función DeleteExtractedFiles elimina los archivos extraídos por la función Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660493"
---
# <a name="deleteextractedfiles-function"></a>DeleteExtractedFiles función)

\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]

La función **DeleteExtractedFiles** elimina los archivos extraídos por la función [**Extract**](extract.md) .

## <a name="syntax"></a>Sintaxis


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PS* 
</dt> <dd>

Puntero a una estructura de [**sesión**](session.md) que contiene información sobre la sesión actual.

Esta función libera la memoria en el miembro **pFileList** de esta estructura y establece **pFileList** en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extracción**](extract.md)
</dt> <dt>

[**SESIÓN**](session.md)
</dt> </dl>

 

 
